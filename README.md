![Repository Banner](header_image.png)
#### Please read [`contributing guidelines`](./contributing.md) before submitting new resources.

## Table of Contents

- [Ruby on Rails Commands](#ror-commands)
- [Ruby on Rails Development gems](#ruby-on-rails-gems)
- [Colors](#colors)
- [Icons](#icons)


## Ruby on Rails Commands

>Websites that offer free fonts as well as font based tools

| CMD&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Description |
| ----------------------- | ------------------ |
| rails new myapp --database=postgresql| rails db as postgress |
| rails new myapp -d mysql| rails db as mysql |
| rails new myapp -T| skip test framework  |
| rails new sti --no-test-framework | skip test framework  |
| rails new myapp --skip_webpack_install| wob application without webpack installation |
| rails new my_api --api| Rails application that will be an API server first and foremost,n |
| rails server -b 0.0.0.0| it will bind to all IP addresses on your machine (LAN access) |
| rails s -e production| Rails  app in Production mode  |
| rails c| Rails console mode  |
| DISABLE_DATABASE_ENVIRONMENT_CHECK=1 RAILS_ENV=production rails c| Rails console mode in production  |
| rails db:create | create database |
| rails db:drop| delete database  |
| rails db:setup| this will run scheema then seed  |
| rails db:migrate| this will run migrations generate scheema |
| rails db:rollback STEP=1 | rollback last migration |
| rake db:migrate:down VERSION=20100905201547 | rollback specific migration |
| rails g scaffold Post name:string title:string content:text |Creating a Resource using scaffold|
| rails g model sale/order  |Creating modulizhe model|
| rails g controller users index show delete|Creating a controller with index show show function|
| rails g model YourModel --migration=false|Creating model without migration|
| rails g model Admin --parent=User|Creating subclasses|




<div align="right">
    <b><a href="#table-of-contents">↥ Back To Top</a></b>
</div>

## Ruby on Rails Development gems

>Ruby on Rails usefull gem in development.

| gem&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Description                                                        |
| -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [gem 'bullet' ](https://github.com/flyerhzm/bullet/)                                                            |  To identify    N+1 query                            |
| [gem 'rack-cors'](https://github.com/cyu/rack-cors/)                                                           |  
| [gem 'rack-attack' ](https://github.com/kickstarter/rack-attack/blob/6-stable/README.md/)                                                            |    requests                           |
| [gem 'brakeman' ](https://github.com/presidentbeef/brakeman/)                                                            |    requests                           |
| [gem 'reek' ](https://github.com/troessner/reek/)                                                            |   requests                           |
| [gem 'better_errors' ](https://github.com/BetterErrors/better_errors/)                                                            |    requests                           |
| [ gem 'rubocop-rails' ](https://github.com/rubocop-hq/rubocop-rails/)                                                            |    requests                           |
| [ gem 'factory_bot_rails' ](https://github.com/thoughtbot/factory_bot_rails/)                                                            |    
| [ gem 'strong_migrations' ](https://github.com/ankane/strong_migrations/)                                                            |    requests                           |
| [ gem 'exception_notification' ](hhttps://github.com/smartinez87/exception_notification/)                                                            |    
| [ gem 'slack-notifier' ](https://github.com/stevenosloan/slack-notifier/)                                                            |   requests                           |

| [ gem 'rubycritic' ](https://github.com/whitesmith/rubycritic/)                                                            |   requests                           |




<div align="right">
    <b><a href="#table-of-contents">↥ Back To Top</a></b>
</div>
