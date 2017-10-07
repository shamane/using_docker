# os: ubuntu 16.0.4
# install docker 
sudo apt-get update
sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'
sudo apt-get update
apt-cache policy docker-engine
sudo apt-get install -y docker-engine
sudo systemctl status docker
  docker run hello-world

# remove docker
sudo apt-get purge -y docker-engine
sudo apt-get autoremove -y --purge docker-engine
sudo apt-get autoclean
sudo apt-get purge -y docker-engine docker docker.io docker-ce

# delete containers, data etc.
rm -rf /var/lib/docker

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
