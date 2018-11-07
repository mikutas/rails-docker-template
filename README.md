# README

1. `sudo docker-compose run rails bundle install`
1. `sudo docker-compose run rails rails new . --force --database=postgresql`
1. Add `gem 'webpacker'` to Gemfile
1. `sudo docker-compose run rails bundle install`
1. `sudo docker-compose run rails rails webpacker:install`
1. `sudo chown -R $USER:$USER .`
1. Add following under the `default:` key of config/database.yml
    * `host: db`
    * `username: postgres`
    * `password:`
1. `sudo docker-compose run rails rails db:create`
1. `sudo docker-compose up`
1. Access `localhost:3000`
