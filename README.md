# Makefile-aws-tool-box
Use this file to create Docker image for aws-toolbox

The objective of this project is to run a docker container for aws-toolbox for running aws cli and python3 for AWS 
To use this code you need to follow the below instructions:

Makefile Background:
The Makefile is the key to the build process. In its simplest form, a Makefile is a script for compiling or building the "binaries", the executable portions of a package. The Makefile can also provide a means of updating a software package without having to recompile every single source file 

Make for Windows:
Please find the details in the link
http://gnuwin32.sourceforge.net/packages/make.htm

Make for Linux:
Please find the details in the link
https://www.gnu.org/software/make/


To Run the Make file:

Follow this instructions:

1) Go the folder where Makefile folder is present. Change permission to execute mode
sudo make

This will download necessary components from Makefile
Successfully built 2a2915e8c8a0
Successfully tagged aws-toolbox:latest
Successfully tagged binxio/aws-toolbox:latest

2) sudo make run

root@mymachine:/home/user1/Downloads# sudo make run
docker run -it \
	-v /home/user1/Downloads/:/workdir \
	-v /root:/root \
	-v /var/run/docker.sock:/var/run/docker.sock \
	-p "3000:3000" \
	-p "8000:8000" \
	aws-toolbox

