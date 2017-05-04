# dockerfileComputerDatabase
Contains all the dockerfiles needed for the training-java project


To build & run a docker from a dockerfile do the following:

1) Build a docker:
$ docker build -t <image-name> .

2) Run a docker:
$ docker run -d --name="<container-name>" -p <host-port>:<docker-port> <image-name>


For JavaMaven docker, to exectue mvn do the following:
$ docker run -it --rm --name <container-name> -v "<pom-directory>:/usr/src/mymaven" -w /usr/src/mymaven <image-name> mvn clean install


In order to let tomcat container & mysql prod container communicate
create a network and add both in it.

1) Create network:
$ docker network create <network-name>

2) Connect containers to network:
$ docker run --net=<network-name> ...
or
$ docker network connect <network-name> <container-name>

3) ping container to be sure it worked:
$ docker exec -ti <container-name-A> ping <container-name-B>
