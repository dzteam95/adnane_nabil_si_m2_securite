# DOCKER MERN - API REST PROJECT

:school: This DOCKER MERN API-RESTfull is a project school MBA 1st promotion :books:

## **🎬 Description**

Includes API endpoints handling for the client part:

Authentification (Sign-up & Login)

Posting articles (List, Edit handling)

<br/>

## **🧱 Structure**

In folder server and client we will find a Dockerfile to build the image:

> ./backend/Dockerfile
>
> ./frontend/Dockerfile

In main repository we will find a docker-compose.yml to set containers launching:

> ./docker-compose.yml

<br/>

## **⚙️ Setup Composing**

Dockerfile content:

> **FROM**: Use a lighter version of Node as a parent image
>
> **WORKDIR**: Set the working directory
>
> **COPY**: Copy the current directory contents into the container at /api
>
> **RUN**: install dependencies
>
> **EXPOSE**: Make port XXXX available to the world outside this container
>
> **CMD**: Run the app when the container launches

In docker-compose.yml:

_we will find there the version and the services of deployment_

<br/>

## **:rocket: Install & Deployment**

> :\$ git clone https://github.com/Jekdesign/valsin_jerry_docker_mds_dev1_2020.git

Use docker:

> :\$ **docker-compose up --build** or **docker-compose up -d --build**
>
> _Shutdown if necessary: :\$ docker-compose down_

<br/>

Pactical basic for npm package manager

> ###### First, run the backend
>
> :\$ cd backend/
>
> :\$ npm install
>
> :\$ npm start
>
> ###### Then, run the frontend
>
> :\$ cd frontend/
>
> :\$ npm install
>
> :\$ npm start

<br/>

:memo: Note

Connection db `mongodb://mongodb:27017`

Backend port `https://localhost:8080`

Client access `https://localhost:3000`

<br/>

## **💻 Technologies**

**Mongodb** _(database)_

**Express** _(node.js framework)_

**React** _(front js framework)_

**Node** _(tool javascript environment)_

**Docker** _(CGROUP + Namespace)_

**CGROUP** _(Partitioning ressources - system, memory, networks)_

**Namespace** _(Insulation for the creation of a container)_

<br/>

## **🆙 Registry Docker bonus step**

### Push image to Registry in public

Build images server & client:

> :\$ cd ./backend
>
> backend:\$ docker build -t server:1.0 .

> :\$ cd ./frontend
>
> frontend:\$ docker build -t client:1.0 .

> :\$ docker images or docker images ls

You can see _REPOSITORY_ and _IMAGE ID_ like this:

| REPOSITORY | TAG | IMAGE ID     |
| ---------- | --- | ------------ |
| server     | 1.0 | baf5690ac0f2 |
| client     | 1.0 | 4dd67690517e |

> :\$ docker tag baf5690ac0f2 <hubusername>/server:1.0
>
> :\$ docker push <hubusername>/server

> :\$ docker tag 4dd67690517e <hubusername>/client:1.0
>
> :\$ docker push <hubusername>/client

<br/>

You can **pull** them via docker hub:

https://hub.docker.com/repository/docker/jechtech/server

> :\$ docker pull jechtech/server

https://hub.docker.com/repository/docker/jechtech/client

> :\$ docker pull jechtech/client
