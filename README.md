Install Docker
$ sudo apt install docker.io
Build docker image
$ sudo docker build -t {image name}
Test docker image, '-p' means allow docker application port 80 porting to host machine port 4000
$ sudo docker run -p 4000:80 {image name}
Run docker image under background 
$ sudo docker -d -p 4000:80 {image name}
Check running docker status
$ sudo docker ps
Stop running docker 
$ sudo docker stop {container ID}
Login docker cloud to prepare upload docker image, must to registry a docker cloud account first
$ sudo docker login 
Give docker image a name and tag
$ sudo docker tag {user name}/{repository}:{tag}
Upload docker image to the docker cloud
$ sudo docker push {user name}/{repository}:{tag}