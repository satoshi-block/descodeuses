# Exercises for Les Descodeuses

## Exercise I 

A/ Install docker system on your local machine

B/ Create a directory on your local machine as follows : (FirstName)_(NameOfYourFavoriteFruit)_codeuses

C/ Into the folder created above, create a Dockerfile which contains all required instructions to start a jenkins server on your local machine
- Tips : Your Dockerfile looks like this : 
```shell
FROM jenkins/jenkins:lts

# if we want to install via apt
USER root
RUN apt-get update && apt-get install -y ruby make

# drop back to the regular jenkins user - good practice
USER jenkins

```

C/ Start building your Dockerfile
- Tips : Use the docker build.... command

D/ Run your jenkins docker container
- Tips : Use the docker run.... command

Caution : take into account that your jenkins is listening on port 8080 inside the container.

Also the port 50000 can be added wihile running your container if you intend to attach a jenkins node agent

E/ Ensure that your jenkins docker container is up and running on local
- Tips : Use the docker ps.... command

F/ Open your browser and check that your jenkins server is up and running and it's reachable at :
- http://(your-ip-address):8080 

or

- http://localhost:8080

G/ Once jenkins starts for the first time, it requires an admninistrator password ... Here find a way to retrieve this password inside the conatiner
- Tips : Use docker exec -ti.... command to log into the container

