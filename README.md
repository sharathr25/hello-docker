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
`docker start -i id_of_image(1st 3 letters)` -> used to run built or pulled images with interactive mode <br />
`docker ps` -> used to check running containers <br />
`docker ps -a` -> used to check running and stopped containers <br />
`docker exec -it -u user_name container_id bash` -> used to run bash session in the container, if don't give user name you will login as root<br />

linux
------
In linux we have package manager 'apt' to install packages like nano, vi etc <br />
apt-get is also there <br />
apt stands for Advanced Package Tool <br />

`apt list` -> to get available packages that can be installed <br />
`apt update` -> to update package database in your ubuntu machine so that you can install packages, <br />
               If you get 'Unable to locate package package_name' then you can update the database by running the command and you can install the package. <br />
`apt install package_name` -> to install a package ex: apt install nano <br />
`touch file_name_1 file_name_2` -> used to create files <br />
`cd path` -> used to get into a folder <br />
`mkdir dirctory_name` -> used to create a directory<br />
`ls` -> used to list files<br />
`ls -number` -> used to list with specified number of files in a line ex: ls -1<br />
`ls -l` -> long listing of files<br />
`mv source_file destination` -> used to move files(rename as well)<br />
`rm file_1 file_2` -> to remove files<br />
`rm file*` -> to remove files with pattern matching<br />
`rm -r directory_name` -> to remove a directory<br />
`nano file_name` -> to edit files<br />
`cat file_name1 file_name1` -> to view file content with concatenation(suits for small files)<br />
`more file_name` -> to view file content(suits for large files, note - we can only scroll down)<br />
`less file_name` -> to view file content(suits for large files, note - we can scroll up and down)<br />
`head -n number_of_lines file_name` -> to see 1st number_of_lines<br />
`tail -n number_of_lines file_name` -> to see last number_of_lines<br />
`cat file_name > file_name2` -> redirection and this can be used with other commands as well<br />
`cat file_name >> file_name2` -> to concate contents and this can be used with other commands as well<br />
`grep pattern options file_name or directory` -> used to search text in files, if we need to search a direcory we need to give -r as option<br />
`find directory -type f -name file_name` -> used to case sensitive sesearch a file <br />
`find directory -type f -iname file_name` -> used to case insensitive sesearch a file <br />
`find directory -type d file_name` -> used to get all the directories in the specified directory <br />
`command_1;command_2;....command_n` -> used to execute multiple commands in one go<br />
`command_1 && command_2 && ....command_n` -> used to execute multiple commands in one go untill one fails<br />
`command_1 || command_2` -> used to execute eiether one of the command<br />
`command_1 | command_2` -> pipe the o/p of command_1 to command_2
`printenv` -. used to see env variables
`printenv env_var_name` -> used to see a perticuler env variable
`echo $env_var_name` ->used to see a perticuler env variable
`export env_name=value` ->used to set a env variable, ex: export A=a
`ps` -> to see list of processes
`kill pid` -> used to kill a process with pid
`useradd` -> used to add users
`adduser` -> used to add users in an interactive mode
`usermod` -> used to modify users
`userdel` -> used to delete users
`groupadd` -> used to add groups 
`groupmod` -> used to modify groups
`groupdel` -> used to delete groups
`chmod` -> used to change permissions of a file