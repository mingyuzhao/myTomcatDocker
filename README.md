myTomcatDocker
======================
Quick environment for developing Web applications.

Author: Ming Zhao ming@stagwell.tech

Requirements
------------
Docker

Configuration
---------------
In “config.json”, you can set the port and endpoints of API services, as well as WSO2 IS params.

Installation
------------
docker build -t user-profile-api . 

docker run -it --rm --name running-user-profile-api -p 8888:8888 user-profile-api

Testing
-----------
Given:

Docker IP: 192.168.99.100 

Host IP:  192.168.0.38


Then:

curl -H "Content-Type:text/plain" -X POST -d '{"role":"admin","scope":"default","userId":"admin","password":"admin","grantType":"password"}' http://192.168.99.100:8888/oauth2Tokens

curl -H "Content-Type:text/plain" -X POST -d '{"accessToken":"d16c2dda73b7a8467e3721dfa78f2f08","tokenType":"Bearer","userId":"admin", "userPassword":"admin"}' http://192.168.99.100:8888/tokens

curl -H "Content-Type:text/plain" -X POST -d '{"userId":"hasinitgh3","password":"hasinitgh","familyName":"gunasingheh","givenName":"hasinitgc", "primaryEmail":"abc@gmail.com", "primaryEmailType":"home", "secondEmail":"abc_temp@gmail.com", "secondEmailType":"work"}' http://192.168.99.100:8888/users

curl -H "Content-Type:text/plain" -X PUT -d '{"userId":"hasinitgh3","password":"abcde","familyName":"li","givenName":"quan", "primaryEmail":"ABC@gmail.com", "primaryEmailType":"home", "secondEmail":"abc_temp@gmail.com", "secondEmailType":"work"}' http://192.168.99.100:8888/users/d2a306e2-7a28-42d9-a907-34f6619e9a44

curl -H "Content-Type:text/plain" -X DELETE http://192.168.99.100:8888/users/d2a306e2-7a28-42d9-a907-34f6619e9a44


Resources
---------
* [Docker](http://www.docker.com)


