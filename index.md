---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---

# Bootstrap Sass Jekyll Template for Github pages

Jekyll Bootstrap template for :octocat: Github pages ([Official Sass version](https://github.com/twbs/bootstrap-sass)). No plugins needed!  It also utilizes many best practices from `minima` theme, checkout the [demo](https://mdrmike.github.io/jekyll-theme-gh-bootstrap/).

**Note:** :book: There are a few known configuration :bug: issues due to Jekyll sass-converter and bootstrap sass requirements.  The results work fine :rocket:, at least for most Bootstrap features, but it's worth :school: understanding [Configuration & Usage](https://github.com/twbs/bootstrap-sass/blob/v3.3.7/README.md) in the TWBS README.

### Setup

1.  Get a copy of this [repository]({{ site.github.repository_url }})
1.  Open the project folder
1.  Setup Bundler & Jekyll
1.  Use bundler to configure your system for the project
1.  Open your favorite text editor
1.  Run the Jekyll server
1.  Browse to [http://localhost:4000](http://localhost:4000)

#### Shell Commands

```sh
git clone {{ site.github.clone_url }}
cd {{ site.github.project_title }}
gem install jekyll bundler
bundle install
atom .
bundle exec jekyll serve
```

## Customize

-   `Gemfile` is used by `bundler` package manger to setup local environment.
-   `_config.yml` is used by to setup jekyll and plugins (or override default) `site.` variables, and define defaults.  The syntax is standard YAML.
-   `_data` folder will be used for menus, social plugins, and other "data" elements.
-   To customize the style, look in `assets`.  `style.scss` has info about how Jekyll uses sass.  Changes should be done in `assets/_sass_imports/theme.scss` or `theme/_custom.scss` and `theme/_theme_variables.scss`
-   Jekyll is made up of two defaults content types.  `pages` are for static content. `posts` are for periodic content, like a blog.  `collections` can be defined to add new content types, and can make use of `_data`.  All can take advantage of `tags` & `categories`.
-   Customize static pages such as `index.md`, `about.md` then add/delete files in `_posts`

## Bugs and Issues

Find a bug or have a suggestion? [Open a new issue]({{ site.github.issues_url }}) on GitHub.
