# caesar-cipher

This repo is used by a Jenkins pipeline (Junit tests). Cf Jenkinsfile

docker-compose.yml for Jenkins :

```
version: '3.7'
services:
  jenkins:
    image: jenkins/jenkins:lts
    privileged: true
    user: root
    ports:
      - 8080:8080
      - 50000:50000
      - 8081:8081
    container_name: jenkins
    volumes:
      - ./jenkinsfolder:/var/jenkins_home
      - /var/run/docker.sock:/var/run/docker.sock
      - /usr/local/bin/docker:/usr/local/bin/docker
 ```


