source 'https://rubygems.org'

ruby '2.1.3'

gem 'rails', '~> 4.1.7'

group :production do
  gem 'rails_12factor'
  gem 'fog', git: 'https://github.com/fog/fog.git', branch: 'master'
  gem 'a9s_swift' # a9s swift utilities
end

gem 'coffee-rails'
gem 'jquery-rails'
gem 'paperclip'
gem 'pg'
gem 'sass-rails'
gem 'uglifier'

group :development, :test do
  gem 'rspec-rails'
  gem 'sqlite3'
  gem 'launchy'
end

group :test do
  gem 'capybara'
  gem 'shoulda-matchers'
end
