# Hello Rails on Docker

## Run
- `docker-compose build`
- `docker-compose up`

### after you change something
-  `docker-compose run web bundle install`
- `docker-compose up --build`

### production
- copy config/master.key (this file is ignored from git)
- `docker-compose -f docker-compose.production.yml build`
- `docker-compose -f docker-compose.production.yml up -d`

## Development
- generate Home controller `docker-compose run web rails g controller Home`



## Reference
- [Quickstart: Compose and Rails | Docker Documentation](https://docs.docker.com/samples/rails/)