# DockerFile

## DockerFile Commands

Command 					| 	Info
---------------   | 	---------------------------------------
`FROM`  			    | 	Must be the first command in a Dockerfile. This command we set the image that will be used as base in our image.
`ADD`  			      | 	To move a file into a container directory. It can be .tar files.
`COPY`  				  | 	Similar to ADD, but you can copy normal files and directories.
`CMD`  						| 	It defines a command to be executed when a container with this image initializes. There can be only one CMD instruction in a Dockerfile. If you add more than one, only the last will take effect.
`LABEL`  					| 	Use it to set a container's description and keep it easy to manage all containers.
`ENTRYPOINT`  		| 	It's like CMD, but this can not be overwritten, it will always execute, the container will run as an executable. When this command dies, the container dies too.
`ENV`  						| 	Sets environment variables to the container.
`EXPOSE`  				| 	Sets ports that container will expose, so that container will be accessible by this ports.
`RUN`  						| 	Used to run commands in the container, generally used to install packages. Each RUN creates a new layer in our container, so we need to avoid creating too many RUN, to create fewer layers and don't let all too messy, after all, we only have read-write access in the last layer, so depending on what we want to do, we can't (e.g. apt-get clean in another RUN).
`USER`  					| 	To define a user inside the container, the default is the ROOT user.
`WORKDIR`  				| 	Defines the directory of work. As the container gets executed, this is the directory that we will get inside when we access the container.
`VOLUME`  				| 	Creates a volume, a directory that will have a copy in our machine/host-docker. Changing something in that volume in our machine will reflect the container, and vice-versa.
`MAINTAINER`  		| 	Set the container owner. (Deprecated)

## DockerFile Build Image

`docker build -t my_image:1.0 .` 
