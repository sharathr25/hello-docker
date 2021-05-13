docker file terminology
-----------------------
`FROM 'base image tag'` -> used to get the base image so that we can run commands
for ex to run js files we need node so we can get node:alpine base image
you can check available docker base iamges in https://hub.docker.com/. <br />
ex: FORM node:alpine

`COPY 'source' 'destination'` -> used to copy files in our machine into docker image file system of base image
source = path of files in our machine <br />
destination = path need to be craeted in file system of docker base image <br />
ex: `COPY . /app`

WORKDIR 'path' -> used to get into a directory in the file system of base image directory.
ex: `WORKDIR /app`

CMD 'cmd' -> used to execute commands
ex: `CMD node app.js`

docker commands
---------------
`docker version` -> to check client ans server verison <br />
`docker build -t tag_name path_where_we_have_docker_file` -> used to build docker image <br />
`docker images` -> to list images <br />
`docker run tag_name` -> used to run built or pulled images, NOTE: if an image with tag_name <br />
                       is not there in the local machine then docker will pull this from docker hub <br />
`docker run -it tag_name` -> used to run built or pulled images with interactive mode <br />
`docker ps` -> used to check running containers <br />
`docker ps -a` -> used to check running and stopped containers <br />


linux
------
In linux we have package manager 'apt' to install packages like nano, vi etc <br />
apt-get is also there <br />
apt stands for Advanced Package Tool <br />

`apt list` -> to get available packages that can be installed <br />
`apt updaete` -> to update package database in your ubuntu machine so that you can install packages, <br />
               If you get 'Unable to locate package package_name' then you can update the database by running the command and you can install the package. <br />
`apt install package_name` -> to install a package ex: apt install nano <br />
