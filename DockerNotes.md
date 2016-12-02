

docker attach <container_id or name> : will get u inside the container
docker inspect <container_id> | grep IPA
docker run -d --name= <Name of Container>
docker run -d --name = <Name> --link <virtual_container_name>:<actual_containername>





Persistant Volume:

-v /data --> Container will stored all the data on data dir
/var/lib/docker/volume

Select the image and you can find the persistant file

Attached a target directory in my local machine : 

docker run -ti -v /app/data:/data --name=aa <image>





Docker Compose:
---------------

Monolithic application(like SaaS) can be broken by docker compose

WeaveScope for management 

docker-compose up
docker-compose <service_name> scale=3
docker-compose down
docker-compose ps
