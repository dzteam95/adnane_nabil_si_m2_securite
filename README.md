securite project 

## **🎬 Description**

Includes API endpoints handling for the client part:

Authentification (Sign-up & Login)

Posting articles (List, Edit handling)

<br/>

## **🧱 Structure**


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

> :\$ git clone 

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

Connection db 

Backend port 

Client access 

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



