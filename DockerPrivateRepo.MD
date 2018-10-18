How to Register a Docker Private Repository
===================================

## Initial set up
Create a file named `daemon.json` under `/etc/docker` with below entry  
`{ "insecure-registries":["<REPO_HOST>:<REPO_PORT>"] }`

## Instruction for Private Repository
Here are the steps to create a docker private repository , push the images, pull the images and run it.

Steps:
---
- Pull the Docker registry images from docker hub  
	`docker run -it -d -p 5000:5000 -v path/to/persitant_storage:/var/lib/registry registry`  
	e.g.  
		`docker run -it -d -p 5000:5000 -v /opt/Registry:/var/lib/registry registry`  
-  Tag a repository  
	 `docker tag container_id dns_private_repo:port/repo_name:tag_name`  
	 `docker tag 2b5e62cacc1b ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx:ALL`  
- Check the tag the repo on docker images  
	 `docker images`  
	 You could see a repo like `ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx`  
- Push the repo into private repository  
     `docker push repo_tag_name`  
     e.g  
     `docker push ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx`  
- Pull the repository from private repository  
    `docker pull reponame:tag_name`  
    e.g <br />
	`docker pull ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx:ALL` <br />
