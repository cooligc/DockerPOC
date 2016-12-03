FROM       centos

MAINTAINER sitakant

ADD mongo.repo /etc/yum.repos.d/

RUN yum upgrade -y

RUN yum install -y mongo-10gen mongo-10gen-server

# Create the MongoDB data directory
RUN mkdir -p /data/db

# Expose port 27017 from the container to the host
EXPOSE 27017 28017

# Set usr/bin/mongod as the dockerized entry-point application
CMD ["mongod"]
