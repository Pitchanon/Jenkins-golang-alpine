# Jenkins Golang alpine

* [Docker Hub]

## Components

* Base: alpine **3.4**
* Jenkins (version: **2.7.3**)
* Go (version: **1.7**)

## Running & Building

### Running

```sh
$ docker run --name=jenkins --rm -it -p 8001:8080 -p 2201:22 -p 50001:50000 -v $(pwd)/var/jenkins_home:/var/jenkins_home -v $(pwd)/root/.ssh:/root/.ssh pitchanon/jenkins-golang-alpine 
```

Run container in background

```sh
$ docker run --name=jenkins -d -it -p 8001:8080 -p 2201:22 -p 50001:50000 --restart=always -v $(pwd)/var/jenkins_home:/var/jenkins_home -v $(pwd)/root/.ssh:/root/.ssh pitchanon/jenkins-golang-alpine 
```

### Building

```sh
$ docker build -t my-jenkins-app .
$ docker run --name jenkins -it --rm -p 8001:8080 -p 2201:22 -p 50001:50000 -v $(pwd)/var/jenkins_home:/var/jenkins_home -v $(pwd)/root/.ssh:/root/.ssh my-jenkins-app
```

### Docker Compose

```sh
$ docker-compose up --build -d
```

### Localhost
* [http://localhost:8001]

[Docker Hub]: https://hub.docker.com/r/pitchanon/jenkins-golang-alpine/
[http://localhost:8001]: http://localhost:8001
