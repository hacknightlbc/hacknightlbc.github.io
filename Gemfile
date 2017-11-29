source 'https://rubygems.org'
ruby RUBY_VERSION
# Gemfile is used by `bundler` package manger to ensure dependencies are met

# This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# gem 'jekyll', '3.2.1'


# Add gems to jekyll_plugins group
# Use github-pages gem to ensure local development mirrors Github pages.
#       Github-pages: https://github.com/github/pages-gem
#       List of gems included: https://pages.github.com/versions/
#
# To use any of these gems, be sure to add to `_config.yml`
#       For example, `jekyll-sitemap` is enabled by default.
gem 'github-pages', group: :jekyll_plugins

# frozen_string_literal: true
source "https://rubygems.org"

# gem "rails"

gem "jekyll"
gem "jekyll-feed"
gem "jekyll-seo-tag"

# Add gems to development group
# A few suggested gems for local development or when not using github pages
#     To use, uncomment, then run `bundle install [--with=GROUP[ GROUP...]]`
#     --with=<list> is A  space-separated  list of groups referencing gems to
#        install. If an optional group is given it is installed. If a group is
#        given that is in the remembered list of groups given to --without, it
#        is removed from that list.
#
# Example: bundle install --with development
#gem 'jekyll-admin', require: false, group: :development
gem 'bootstrap-sass', require: false, group: :development
# Add to older version of sass to development group to ensure its available when
# generating sourcemaps using compass 1.0.3 (:bug: with 3.5.x branch)
# see `assets/style.scss` for details
gem 'sass', '~> 3.4.25', group: :development

# Add gems to travis group
# About Travis CI: http://jekyllrb.com/docs/continuous-integration/
#gem 'html-proofer', group: :travis
#gem 'scss_lint', require: false, group: :travis

# If you have any plugins, put them here!
group :jekyll_plugins do
end

group :travis do
end

group :development, optional: true do
end
