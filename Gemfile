source "https://rubygems.org"
ruby RUBY_VERSION

# Hello!
#
# After cloning HacknightsLBC locally, you need to setup your local environment.
# Do this to insure your local gems (and versions) match what's on Github
# To setup (or update) your environment to match Github, do this:
#
#     bundle install
#
# This will help ensure the proper Jekyll version is running.
#
# To serve the site for local testing, do this:
#
#     bundle exec jekyll serve
#
#
#
# Additional Notes
# =====
# Because HacknightsLBC is hosted on Github, it requires the github-pages gem
# Github does not support any other jekyll plugins.
#
# To find out what plugins are included in github-pages, that you can use
# in the _config.yml file, visit:
# https://pages.github.com/versions/
#
#
#  To Use the Optional Development Gems, do this:
#
#     bundle install --with development
#
#  Happy Jekylling!

gem "github-pages", group: :jekyll_plugins

 group :jekyll_plugins do
 end

 group :development, optional: true do
   gem 'jekyll-admin', require: false
   gem 'editorconfig', require: false
 end
