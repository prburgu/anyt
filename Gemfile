# frozen_string_literal: true

source "https://rubygems.org"

gem "pry-byebug", platform: :mri

eval_gemfile "gemfiles/rubocop.gemfile"

# Specify your gem's dependencies in anyt.gemspec
gemspec

if File.directory?(File.join(__dir__, "../anycable"))
  $stdout.puts "\n=== Using local AnyCable gems ===\n\n"
  path ".." do
    gem "anycable"
    gem "anycable-rails"
  end
else
  gem "anycable", ">= 1.0.0"
  gem "anycable-rails", ">= 1.0.0"
end
