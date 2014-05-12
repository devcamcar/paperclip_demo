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

    $ bundle exec rake db:create db:migrate

Run the rails server

    $ bundle exec rails s

### View Application

From a web browser access the site via [localhost:3000](http://localhost:3000)

## Deploy the application to Anynines

### Service Dependencies

+ PostgreSQL service
+ Anynines Swift service

### Ruby cli (v5)

Install the a9s gem

    $ gem install a9s

Edit the deployment manifest

    $ cp manifest.yml.example manifest.yml
    $ vim manifest.yml # exchange all occurences of app_name with your desired application identifier

Deploy the application

    $ cf push

### Go cli (v6)

Install the cf go cli: https://github.com/cloudfoundry/cli/releases

Edit the deployment manifest

    $ cp manifest.yml.v6 manifest.yml
    $ vim manifest.yml # exchange all occurences of app_name with your desired application identifier

Create the needed services

    $ cf create-service postgresql Pluto-free postgresql-app_name
    $ cf create-service swift free swift-app_name

Deploy the application

    $ cf push
    
Visit the application url: http://app_name.de.a9sapp.eu .


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
