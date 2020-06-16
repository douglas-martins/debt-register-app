<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcR-LnkQEQ3fRh4n8Y1fWh9wLbdUZnnkoQ13tkwHKwwed8lKgwZ_&usqp=CAU"  alt=""/>
<img src="https://d1q6f0aelx0por.cloudfront.net/product-logos/644d2f15-c5db-4731-a353-ace6235841fa-registry.png"  alt=""/>

# Debt Register App


Full web application building on a Docker Container:
- [Backend: (NodeJS + Express + MongoDB)](https://github.com/douglas-martins/debt-register-api)
- [Web Client: (Angular v9.x)](https://github.com/douglas-martins/debt-register-web-client)

--- 
### Docker
#### Docker installation on:
- [Windows](https://docs.docker.com/docker-for-windows/install/)
- [Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
- [macOs](https://docs.docker.com/docker-for-mac/install/)

--- 
### Docker Compose
#### Docker Compose installation on:
- [All Platforms](https://docs.docker.com/compose/install/)

--- 
## Config Docker container to run application 



### Get repository sub modules 

```bash
$ git clone https://github.com/douglas-martins/debt-register-app.git
$ cd debt-register-app
$ git submodule init && git submodule update

# to update all submodules:
$ git submodule update --recursive --remote
```

### Init Backend

```bash
$ cd debt-register-api
$ git checkout master
$ git pull
$ yarn install

# Copy the base file for the environment one (from the / for this project)
$ cp .env_base .env

# Value for .env
APP_VERSION=1.0.0
HOST=0.0.0.0
PORT=3000
DATABASE_HOST=database
DATABASE_PORT=27017
DATABASE_NAME=debts
```

### Init Web Client

```bash
$ cd debt-register-web-client
$ git checkout master
$ git pull
$ yarn install
```

### Init Docker container

```bash
$ docker-compose build
$ docker-compose up
# or (for running in background)
$ docker-compose up -d
```
