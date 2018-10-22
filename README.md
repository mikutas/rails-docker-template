# README

1. `sudo docker-compose run rails rails new . --force --database=postgresql`
1. Add `gem 'webpacker'` to Gemfile
1. `sudo docker-compose build rails`
1. `docker-compose run rails rails webpacker:install`
1. `docker-compose stop`
1. `sudo chown -R $USER:$USER .`
1. Add following to config/database.yml

```
default: &default
  host: db
  username: postgres
  password:
```

1. `docker-compose run rails rails db:create`
1. `sudo docker-compose build`
1. `docker-compose up`
1. Access `localhost:3000`
