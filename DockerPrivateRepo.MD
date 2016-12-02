How to Register a Docker Private Repository
===================================

Here are the steps to create a docker private repository , push the images, pull the images and run it.

Steps:
- Pull the Docker registry images from docker hub <br />
	`docker run -it -d -p 5000:5000 -v path/to/persitant_storage:/var/lib/registry registry` <br />
	e.g. <br />
		`docker run -it -d -p 5000:5000 -v /opt/Registry:/var/lib/registry registry` <br />
-  Tag a repository <br />
	 `docker tag container_id dns_private_repo:port/repo_name:tag_name` <br />
	 `docker tag 2b5e62cacc1b ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx:ALL` <br />
- Check the tag the repo on docker images <br />
	 `docker images` <br />
	 You could see a repo like `ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx` <br />
- Push the repo into private repository <br />
     `docker push repo_tag_name` <br />
     e.g <br />
     `docker push ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx` <br />
- Pull the repository from private repository <br />
    `docker pull reponame:tag_name` <br />
    e.g <br />
	`docker pull ec2-52-91-228-173.compute-1.amazonaws.com:5000/nginx:ALL` <br />
