# Steps to install Docker in RHEL

All the <b>steps</b>to be done using ROOT previlage <br/>


- sudo yum update <br/>

- tee /etc/yum.repos.d/docker.repo <<-'EOF' <br/>
    [dockerrepo] <br/>
    name=Docker Repository <br/>
    baseurl=https://yum.dockerproject.org/repo/main/centos/7/ <br/>
    enabled=1 <br/>
    gpgcheck=1 <br/>
    gpgkey=https://yum.dockerproject.org/gpg <br/>
    EOF <br/>

<br />
- yum install docker-engine <br />


- systemctl enable docker.service <br />


- systemctl start docker <br />







