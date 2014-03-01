## Paperclip Demo

### Reference Application

![Paperclip Demo Application](https://s3.amazonaws.com/paperclip_demo/paperclip_demo_screenshot_470.png)

Application allows users to manage a list of “friends” using a basic Rails scaffold. Each friend will have a Name and Avatar. Paperclip will provide the image upload and resizing functionality. The app will demonstrate how to create different sized thumbnails, display resized images on different screens, and gracefully degrade to display missing avatars “missing.png” for friends without an avatar.

### Install Codebase

Clone the git repository

    $ git clone git@github.com:anynines/paperclip_demo.git
    $ cd paperclip_demo
    $ bundle

Create database and run migrations

    $ rake db:create db:migrate

Run the rails server

    $ rails s

### View Application

From a web browser access the site via [localhost:3000](http://localhost:3000)

## Deploy the application to Anynines

Precompile the assets locally to speed up the process

    $ bundle exec rake assets:precompile

Install the a9s gem

    $ gem install a9s

Edit the deployment manifest

    $ vim manifest.yml -> exchange all occurences of app_name with your desired application identifier

Deploy the application 

    $ cf push

## Test suite

RSpec and Capybara used for Integration and Unit tests

    $ rspec
    
Credits
-------

![thoughtbot](http://thoughtbot.com/images/tm/logo.png)

Paperclip Demo is maintained by [thoughtbot, inc](http://thoughtbot.com/community)

The names and logos for thoughtbot are trademarks of thoughtbot, inc.

License
-------

Trail Map is licensed under the [Creative Commons Attribution License](http://creativecommons.org/licenses/by/3.0/).
