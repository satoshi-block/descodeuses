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

G/ Once jenkins starts for the first time, it requires an admninistrator password ... At this stage, find a way to retrieve this password inside the container
- Tips : Use docker exec -ti.... command to log into the container

## Exercise II

A/ Once connected to jenkins, start installing docker plugin by browsing this url : http://(localhost OR IP-Address):8080/pluginManager/available?filter=Cloud+Providers

Check 'Docker' plugin as shown above and click on 'install without restart' button

B/ Create your first jenkins pipeline job by clicking on "Create a job"

- Enter a jenkins job name : myFirstPipeline

- Select pipeline as option

- Validate by clicking on OK button






