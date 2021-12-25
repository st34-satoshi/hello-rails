# Hello Rails on Docker

## Run
- `docker-compose build`
- `docker-compose up`

### after you change something
-  `docker-compose run web bundle install`
- `docker-compose up --build`

### production
- copy config/master.key (this file is ignored from git)
    - or you can recreate credentials.yml.enc and master.key: 
        - `rm config/credentials.yml.enc`
        - `docker-compose run -e EDITOR=vim web rails credentials:edit`
- `docker-compose -f docker-compose.production.yml build`
- `docker-compose -f docker-compose.production.yml up -d`

## Development
- generate Home controller `docker-compose run web rails g controller Home`
- migrate the db `docker-compose run web rails db:migrate`
- install js packages using yarn `docker-compose run web yarn add package-name`



## Reference
- [Quickstart: Compose and Rails | Docker Documentation](https://docs.docker.com/samples/rails/)