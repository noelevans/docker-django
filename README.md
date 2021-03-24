# docker-django
Following the Hello World example for Djanjo on Docker.

The services being created are defined in docker-compose.yml. This file also contains arguments to be passed to each service.

## Alpine requirements
py-pip
python3-dev
libffi-dev
openssl-dev
gcc
libc-dev
rust
cargo
make

## Install Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.28.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo pacman -Syu docker
systemctl enable docker.service
systemctl start docker.service

## Setup Django project
sudo docker-compose run web django-admin startproject composeexample .

## Running the application
The dev environment has all its settings in env.dev
Run the application with these settings using:
    `docker-compose --env-file env.dev up`
