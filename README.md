# hacknightlbc.github.io
Uncoded Hack Night - Long Beach, CA

Welcome to our site repo.

We are in the process of making it easier to edit or contribute to the site.
Currently if you would like to build an instance on your local machine with docker follow along:

## Step one (1)
Clone this repo in a directory of your choice (@poproar prefers a subdirectory in /home/user like ~/Jekylls)
```git clone https://github.com/hacknightlbc/hacknightlbc.github.io.git```

## Step two (2)
Go into the newly cloned directory
```cd hacknight.githublbc.io```

## Step three (3)
Ensure the entrypoint file is executable
```chmod +x docker-entrypoint.sh```

## Step four (4)
Build a docker image (you can name it anything you want @poproar used jekyllHackNight for clarity)
```docker build --force-rm -t jekyllHackNight .```

## Step five (5)
Run your container (@poproar used port 4000 for his own sanity but you could use any port like 80:4000)
```docker run --rm -p 4000:4000 -v $(pwd):/site jekyllHackNight```

## Step six (6)
Point your browser to [localhost:4000](http://localhost:4000) or just [localhost](http://localhost) if you used port 80

## Step seven (7)
Enjoy

### Thanks
A big thanks goes to @BretFisher for sharing this [repo](https://github.com/BretFisher/jekyll-serve) to get us started.
Not sure how to fork and suggest the Dockerfile changes made here to get github-pages gem to work
