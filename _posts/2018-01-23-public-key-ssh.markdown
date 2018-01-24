---
title: Public / Private Key Encryption with SSH
layout: post
---
To wrap our heads around the concept of the key access let's go over some of the basics.

**From [Wikipedia]**: Secure Shell (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network. The best known example application is for remote login to computer systems by users.

The idea is that one machine (Client) can remotly call another machine (Server) and share an encrypted connection. This connection was similar to telnet but with the added security of cryptographic security.

## Public and Private key

By default most SSH servers are only secured by a username and password. That's not the most secure system as it can be brute-forced. There are bots on the web that dig around for unpached SSH servers with default [logins still enabled].

Using a public / private key solution is far more secure.

By default when we generate a ssh-key it outputs a `id_rsa` and an `id_rsa.pub` file. To automattically have the host accept the cliet's key the contents of `id_rsa.pub` should be in the hosts' `authorized_keys` file. These are all text files so the `authorized_keys` file can have multible lines equating to devices.

## Getting it down

On the host we need to generate the key.

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

It will ask you for a password. It's highly recomended. Serices like Github won't work without a password. It'll also ask what to name the files but `id_rsa` is probably the best.

There are few high tech solutions to sending the public key to the host but I usually push it through ssh or on a thumb drive. Once the public key is on the host, from the host session run:

`cat id_rsa.pub >> .ssh/authorized_keys`

This will add the key to the end of the authorized key list or generate that file if it's not already there.

## SSHD

Now that everything is all set up with the keys it's time to remove the password logins.

Edit the `sshd_config`:

Change the `PublicAuthentication no` to yes and change:

```
ChallengeResponseAuthentication no
PasswordAuthentication no
UsePAM no
```

The last step is to restart the SSHD server.

System D:  
`sudo systemctl restart sshd`

Init.d:  
`/etc/init.d/sshd restart`

The next time you login everything should connect without a password.

[Wikipedia]: https://en.wikipedia.org/wiki/Secure_Shell

[logins still enabled]: #

