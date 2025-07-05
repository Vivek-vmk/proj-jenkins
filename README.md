### freestyle docs(on instance)

  - goto jenkins dashboard
  - click create new item
  - define your project name
  - select freestyle project
  - mention github project section : your github repo url
  - build now


Deploy :-

`apt install nodejs -y`

`apt install npm -y`

`npm install`

`node app.js`

(If you want to use CI_cd as automatic way , then set-up github-jenkins integration)

### freestyle docs(on container)

`apt install docker.io -y`

  - goto jenkins dashboard
  - click create new item
  - define your project name
  - select freestyle project
  - mention github project section : your github repo url
  - Go to configure --- build step --- execute shell

`docker build -t myimg  .`
`docker run -itd --name cont1 -p 8000:8000 myimg:latest`

  - build now
  - `docker ps -a`

(Delete previous container, `docker kill container name`, `docker rm container name`)

USING COMPOSE :-

`apt install docker-compose -y`

Go to configure --- build step --- execute shell

`docker compose down`
`docker compose up -d`

build now

(If you want to use CI_cd as automatic way , then set-up github-jenkins integration)

-----



### Pipeline docs(on Container)

(Delete previous container, `docker kill container name`, `docker rm container name`)

  - goto jenkins dashboard
  - click create new item
  - define your project name
  - select PIPELINE project
  - mention github project section : your github repo url
  - use jenkins file for docker only
  - build now
  - `docker ps -a`

(Access webapp)


### Pipeline docs(on Container)

(Delete previous container, `docker kill container name`, `docker rm container name`)

`apt install docker-compose -y`

(IMP = ID --> dockerHub, docker-hub username & pw)

  - goto jenkins dashboard
  - click create new item
  - define your project name
  - select PIPELINE project
  - mention github project section : your github repo url
  - use jenkins file for docker-compose only
  - build now
  - `docker ps -a`

(Access webapp)
