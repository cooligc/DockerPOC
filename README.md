# DockerPOC

This repository will have the Dockerfiles that I have created


## Docker Cheat Sheet
1. `docker run -i -t --entrypoint /bin/bash <Image_ID>`  -> Run the docker in bash mode
2. `docker exec -it <Container_id>  bash` -> Execute a docker bash which is running on demon mode
3. `docker images `--> List of stored images
4. `docker build . -t <TAG_NAME>`--> To build from DockerFile
5. `docker search <app_name> `--> Search container from Docker hub
6. `docker rmi <image_id> `--> Delete the image from local repository
7. `docker rmi -f 'docker images -q' `-> Delete all the local repository 
8. `docker ps `--> To see all the ongoing docker process
9. `docker stop $(docker ps -a -q) `-- > Stop the docker container based on their process id
10. `docker run -t -i <container_name> ` -- > To start a container
11. `docker rmi -f $(docker images | grep "<none>" | awk "{print \$3}")` -> Remove docker images having container id <none>
