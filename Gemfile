# encoding: utf-8

source 'https://rubygems.org'

gem 'berkshelf',  '~> 4.0'
gem 'chef',       '>= 12.0'

# pin dependency for Ruby 1.9.3 since bundler is not
# detecting that net-ssh 3 does not work with 1.9.3
if Gem::Version.new(RUBY_VERSION) <= Gem::Version.new('1.9.3')
  gem 'net-ssh', '~> 2.9'
end

group :test do
  gem 'rake'
  gem 'chefspec',   '~> 4.2.0'
  gem 'foodcritic', '~> 4.0'
  gem 'thor-foodcritic'
  gem 'rubocop',    '~> 0.31.0'
  gem 'coveralls',  require: false
  gem 'minitest', '~> 5.5'
  gem 'simplecov', '~> 0.10'
end

group :development do
  gem 'guard'
  gem 'guard-rspec'
  gem 'guard-kitchen'
  gem 'guard-rubocop'
  gem 'guard-foodcritic'
end

group :integration do
  gem 'test-kitchen', '~> 1.0'
  gem 'kitchen-vagrant'
  gem 'kitchen-inspec'
  gem 'kitchen-sharedtests', '~> 0.2.0'
  gem 'concurrent-ruby', '~> 0.9'
  gem 'kitchen-dokken'
end

group :tools do
  gem 'github_changelog_generator', '~> 1.12.0'
end
