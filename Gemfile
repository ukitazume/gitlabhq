source "https://rubygems.org"

def darwin_only(require_as)
  RUBY_PLATFORM.include?('darwin') && require_as
end

def linux_only(require_as)
  RUBY_PLATFORM.include?('linux') && require_as
end

gem "rails", "6.0.3.5"

# Supported DBs
gem "mysql2", group: :mysql
gem "pg", group: :postgres

# Auth
gem "devise", "~> 4.7", ">= 4.7.0"
gem 'omniauth', "~> 1.1.3"
gem 'omniauth-google-oauth2'
gem 'omniauth-twitter'
gem 'omniauth-github'

# Extracting information from a git repository
# Provide access to Gitlab::Git library
gem "gitlab_git", '2.1.1'

# Ruby/Rack Git Smart-HTTP Server Handler
gem 'gitlab-grack', '~> 1.0.1', require: 'grack'

# LDAP Auth
gem 'gitlab_omniauth-ldap', '1.0.3', require: "omniauth-ldap"

# Syntax highlighter
gem "gitlab-pygments.rb", '~> 0.3.2', require: 'pygments.rb'

# Git Wiki
gem "gitlab-gollum-lib", "~> 1.0.1", require: 'gollum-lib'

# Language detection
gem "github-linguist", require: "linguist"

# API
gem "grape", "~> 0.4.1"
gem "grape-entity", "~> 0.3.0"

# Format dates and times
# based on human-friendly examples
gem "stamp"

# Enumeration fields
gem 'enumerize'

# Pagination
gem "kaminari", "~> 0.14.1"

# HAML
gem "haml-rails", ">= 0.5.3"

# Files attachments
gem "carrierwave"

# for aws storage
gem "fog", "~> 1.3.1", group: :aws

# Authorization
gem "six"

# Seed data
gem "seed-fu"

# Markdown to HTML
gem "redcarpet",     "~> 2.2.2"
gem "github-markup", "~> 0.7.4", require: 'github/markup'

# Asciidoc to HTML
gem  "asciidoctor"

# Application server
gem "unicorn", '~> 4.6.3', group: :unicorn

# State machine
gem "state_machine"

# Issue tags
gem "acts-as-taggable-on", ">= 3.1.0"

# Background jobs
gem 'slim'
gem 'sinatra', require: nil
gem 'sidekiq'

# HTTP requests
gem "httparty"

# Colored output to console
gem "colored"

# GitLab settings
gem 'settingslogic'

# Misc
gem "foreman"

# Cache
gem "redis-rails", ">= 5.0.2"

# Campfire integration
gem 'tinder', '~> 1.9.2'

# HipChat integration
gem "hipchat", "~> 0.9.0"

# d3
gem "d3_rails", "~> 3.1.10"

# underscore-rails
gem "underscore-rails", "~> 1.4.4"

# Sanitize user input
gem "sanitize"

group :assets do
  gem "sass-rails", ">= 5.0.8"
  gem "coffee-rails", ">= 4.2.2"
  gem "uglifier"
  gem "therubyracer"
  gem 'turbolinks', '>= 1.2.0'
  gem 'jquery-turbolinks', '>= 1.0.0'

  gem 'chosen-rails', '1.0.0'
  gem 'select2-rails', '>= 3.4.2'
  gem 'jquery-atwho-rails', "0.3.0"
  gem "jquery-rails", "4.0.1"
  gem "jquery-ui-rails", "2.0.2"
  gem "modernizr",        "2.6.2"
  gem "raphael-rails",    git: "https://github.com/gitlabhq/raphael-rails.git"
  gem 'bootstrap-sass'
  gem "font-awesome-rails", ">= 4.7.0.5"
  gem "gemoji", "~> 1.2.1", require: 'emoji/railtie'
  gem "gon", ">= 4.1.1"
end

group :development do
  gem "annotate", git: "https://github.com/ctran/annotate_models.git"
  gem "letter_opener"
  gem 'quiet_assets', '~> 1.0.1'
  gem 'rack-mini-profiler'
  # Better errors handler
  gem 'better_errors'
  gem 'binding_of_caller'

  gem 'rails_best_practices'

  # Docs generator
  gem "sdoc"

  # thin instead webrick
  gem 'thin'
end

group :development, :test do
  gem 'coveralls', require: false
  gem 'rails-dev-tweaks', '>= 1.1.0'
  gem 'spinach-rails', '>= 0.2.1'
  gem "rspec-rails", ">= 2.13.2"
  gem "capybara"
  gem "pry"
  gem "awesome_print"
  gem "database_cleaner"
  gem "launchy"
  gem 'factory_girl_rails', '>= 4.2.1'

  # Prevent occasions where minitest is not bundled in packaged versions of ruby (see #3826)
  gem 'minitest', '~> 4.7.0'

  # Generate Fake data
  gem "ffaker"

  # Guard
  gem 'guard-rspec'
  gem 'guard-spinach'

  # Notification
  gem 'rb-fsevent', require: darwin_only('rb-fsevent')
  gem 'growl',      require: darwin_only('growl')
  gem 'rb-inotify', require: linux_only('rb-inotify')

  # PhantomJS driver for Capybara
  gem 'poltergeist', '~> 1.3.0'

  gem 'spork', '~> 1.0rc'
  gem 'jasmine'
end

group :test do
  gem "simplecov", require: false
  gem "shoulda-matchers", "~> 2.1.0"
  gem 'email_spec'
  gem "webmock"
  gem 'test_after_commit'
end

group :production do
  gem "gitlab_meta", '6.0'
end
