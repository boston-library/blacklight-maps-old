source 'https://rubygems.org'

# Specify your gem's dependencies in blacklight-maps.gemspec
gemspec

gem 'simplecov', require: false
gem 'coveralls', require: false

# If we don't specify 2.11.0 we'll end up with sprockets 2.12.0 in the main
# Gemfile.lock but since sass-rails gets generated (rails new) into the test app
# it'll want sprockets 2.11.0 and we'll have a conflict
gem 'sprockets', '2.11.0'

# # If we don't specify 3.2.15 we'll end up with sass 3.3.2 in the main
# # Gemfile.lock but since sass-rails gets generated (rails new) into the test app
# # it'll want sass 3.2.0 and we'll have a conflict
gem 'sass', '~> 3.2.0'


file = File.expand_path("Gemfile", ENV['ENGINE_CART_DESTINATION'] || ENV['RAILS_ROOT'] || File.expand_path("../spec/internal", __FILE__))
if File.exists?(file)
  puts "Loading #{file} ..." if $DEBUG # `ruby -d` or `bundle -v`
  instance_eval File.read(file)
end
