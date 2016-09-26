myTomcatDocker
======================
Quick environment for developing Web applications.

Author: Ming Zhao mingyu.zhao@gmail.com

Requirements
------------
Docker

Configuration
---------------
In “config.json”, you can set the port and endpoints of API services, as well as WSO2 IS params.

Installation
------------
docker build -t myTomcat . 

docker run -it --rm --name running-tomcat-8 -p 8888:8888 tomcat:8.0

Testing
-----------
Given:

Docker IP: 192.168.99.100 

Host IP:  192.168.0.38


Then:

curl -H "Content-Type:text/plain" -X POST -d '{"role":"admin","scope":"default","userId":"admin","password":"admin","grantType":"password"}' http://192.168.99.100:8888/oauth2Tokens


Resources
---------
* [Docker](http://www.docker.com)


