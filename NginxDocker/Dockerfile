FROM centos

MAINTAINER sitakant

RUN yum update -y

RUN yum install -y wget

RUN yum install -y openssl


RUN wget http://nginx.org/packages/mainline/centos/7/x86_64/RPMS/nginx-1.11.0-1.el7.ngx.x86_64.rpm

RUN rpm -i nginx-1.11.0-1.el7.ngx.x86_64.rpm

COPY index.html /usr/share/nginx/html


EXPOSE 80


CMD ["nginx", "-g", "daemon off;"]
