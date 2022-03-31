source 'https://rubygems.org'
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby '2.5.1'

def host_os_is?(regex)
  RbConfig::CONFIG['host_os'] =~ regex
end

group :core do
  gem 'activerecord-session_store'
  gem 'airbrake'
  gem 'bootsnap', '>= 1.4.2', require: false # Reduces boot times through caching; required in config/boot.rb
  gem 'devise'
  gem 'pg'
  gem 'puma', '~> 4.3'
  gem 'rails', '~> 6.0.2', '>= 6.0.2.1'
end

group :frontend do
  gem 'bootstrap'
  gem 'browser'
  gem 'country_select'
  gem 'font_awesome5_rails'
  gem 'jbuilder', '~> 2.7'
  gem 'jquery-rails'
  gem 'js-routes'
  gem 'sass-rails', '>= 6'
  gem 'simple_form'
  gem 'slim-rails'
  gem 'turbolinks', '~> 5'
  gem 'webpacker', '~> 4.0'
end

group :backend do
end

group :utils do
  gem 'brakeman', '~> 4.3', '>= 4.3.1'
  gem 'bundler-audit'
  gem 'colorize'
  gem 'pluck_to_hash'
  gem 'require_all'
  gem 'terminal-notifier', platforms: :ruby, install_if: host_os_is?(/darwin/)
  gem 'turnout'
end

group :development, :test do
  gem 'byebug', platforms: [:mri]
  gem 'factory_bot_rails'
  gem 'pry'
  gem 'pry-alias'
  #gem 'pry-byebug' # Disabled due to error: uninitialized constant Pry::Command::ExitAll (NameError)
  gem 'pry-rails'
  gem 'pry-rescue'
  gem 'pry-stack_explorer'
  gem 'rubocop', require: false
  gem 'rubocop-rails'
end

group :development do
  gem 'annotate'
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'listen', '>= 3.0.5', '< 3.2'
  gem 'rails-erd'
  gem 'rb-readline'
  gem 'spring'
  gem 'spring-watcher-listen', '~> 2.0.0'
  # Access an interactive console on exception pages or by calling 'console' anywhere in the code.
  gem 'web-console', '>= 3.3.0'
end

group :test do
  gem 'capybara', '>= 2.15' # Adds support for Capybara system testing and selenium driver
  gem 'guard'
  gem 'guard-minitest'
  gem 'm'
  gem 'minitest-focus' # Focus on one test at a time.
  gem 'minitest-macos-notification', platforms: :ruby, install_if: host_os_is?(/darwin/)
  gem 'minitest-optional_retry'
  gem 'minitest-rails', git: 'https://github.com/blowmage/minitest-rails'
  gem 'minitest-spec-rails' # Drops in Minitest::Spec superclass for ActiveSupport::TestCase
  gem 'selenium-webdriver'
  gem 'simplecov', require: false
  gem 'webdrivers'
end

# Use Redis adapter to run Action Cable in production
# gem 'redis', '~> 4.0'

# Use Active Model has_secure_password
# gem 'bcrypt', '~> 3.1.7'

# Use Active Storage variant
# gem 'image_processing', '~> 1.2'
