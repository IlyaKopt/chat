Site Description
----------------
Chaat is an open-source application which creates for real-time commnication with your partners, friends e.t.c. This app executes in HipChat style and has such functionality as:
- creating chat rooms where you have an opportunity to сommunicte with a group of people you add
- chating with person privately
- adding your friends  through email invitation without any limits
- attaching files (documents, images, viedos from youtube)
- every user has his own profile which he can customize


Requirements
-------------

- ruby 2.1.2
- Rails 4.1.1
- PostgreSQL 9.1.13

Getting Started
-------------
There is a couple things you need to start working with Chat on your machine. If  you have been already worked with Ruby environment and has Bundler been installed, you can go to the repository "chat" https://github.com/IlyaKopt/chat.git and clone it via your terminal:

    git clone git@github.com:IlyaKopt/chat.git

- Then change directory to chat and install the gems from 'Gemfile':
```
    cd chat
    bundle install`
```

- Chat is configure to use Pusher. If you need to work it locally, you should to register your app using Pusher and add some Pusher credentials in '.env' file. For example:
```
    Pusher.app_id = 'your-pusher-app-id'
    Pusher.key = 'your-pusher-key'
    Pusher.secret = 'your-pusher-secret'
    Pusher.host   = 'your-host'
    Pusher.port   = 4567
```
- Also you can use Slanger. You need to install Slanger Server
```
    gem install slanger
```
- add Slanger credentials:
```
    slanger --app_key 765ec374ae0a69f4ce44 --secret your-pusher-secret
```
- Chat uses gem OmniAuth for login from Facebook and Github. Add some OmniAuth credentials in '.env' file. For example:
```
    provider :github, 'GITHUB_KEY', 'GITHUB_SECRET'
    provider :facebook, 'FACEBOOK_KEY', 'FACEBOOK_SECRET'
```
- Add 'config/database.yml' file.

- Create database:
```
    rake db:create
```

- Run the database migration:
```
    rake db:migrate
```
- Start the web server:
```
    rails s
```

- Using a browser, go to http://localhost:3000, login and start chatting.

Database
--------

This application uses PostgreSQL with ActiveRecord.

Development
-----------

-   Template Engine: Haml
-   Testing Framework: RSpec and Factory Girl
-   Front-end Framework: Bootstrap 3.0 (Sass)
-   Authentication: Devise


Email
-----

The application is configured to send email using a Gmail account. Add credentials in '.env' file. Example you can get from '.env.example' file.

Chat is made available under the [MIT License](http://www.opensource.org/licenses/mit-license.php).