> sudo docker --version
  Docker version 17.05.0-ce, build 89658be
> sudo docker-compose --version
  docker-compose version 1.16.1, build 6d1ac21

1)
  sudo docker-compose build

2)
  sudo docker-compose run --rm webapp bin/rails db:migrate

3)
  sudo docker-compose up

● In 'master': 
    Ruby on Rails project
    Nginx
    PhusionPassenger

● in 'nginx_puma' branch:
    Ruby on Rails project
    Nginx
    Puma
