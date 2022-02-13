# Docker Commands

## Image Commands

Command 											                        | 	Info
---------------------------------------------------   | 	---------------------------------------
`docker image ls`  							                      | 	List images
`docker create [IMAGE]`  								              | 	Create a container (without starting it)
`docker build [URL]`  								                | 	Create an image from a Dockerfile
`docker build -t [IMAGE_TAG] .`  								      | 	Create an image from a Dockerfile
`docker pull [IMAGE]`  								                | 	Pull an image from a registry
`docker push [IMAGE]`  								                | 	Push an image to a registry
`docker rmi [IMAGE]` 									                | 	Remove an image
`docker commit [CONTAINER] [NEW_IMAGE_NAME]`      		| 	Create an image from a container
`docker save [IMAGE] > [TAR_FILE]`  					        | 	Save an image to a tar archive
`docker load [TAR_FILE/STDIN_FILE]`  					        | 	Load an image from a tar archive or stdin
`docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`    | 	Tag image 

## Container Commands

Command 											                        | 	Info
---------------------------------------------------   | 	---------------------------------------
`docker ps`  									                        | 	List running containers
`docker ps -a`  								                      | 	List all containers
`docker run [IMAGE] [COMMAND]`  						          | 	Run a command in a new container:
`docker run -d -p 80:80 my_image nginx`  						  | 	Run nginx detached mode and port 80:
`docker rm [CONTAINER]`  								              | 	Delete a container (-f with force)
`docker start [CONTAINER]`  				                  | 	Start a container
`docker stop [CONTAINER]`  					                  | 	Stop a running container
`docker restart [CONTAINER]`  			                  | 	Stop a running container and start it up again
`docker rename [CONTAINER_NAME] [NEW_CONTAINER_NAME]` | 	Rename an existing container
`docker cp [PATH] [PATH]`  	                          | 	Copy file from/into the container

## Auth Commands

Command 											                        | 	Info
---------------------------------------------------   | 	---------------------------------------
`docker login`  	                                    | 	Login to a registry
`docker logout`  	                                    | 	Logout from a registry


## Network Commands

Command 											                        | 	Info
---------------------------------------------------   | 	---------------------------------------
`docker network ls`  							                    | 	List networks
`docker network inspect [NETWORK]`  			            | 	Show information on one or more networks
`docker network create [OPTIONS] [NETWORK]` 					| 	Create network
`docker network rm [NETWORK]` 						            | 	Remove one or more networks
`docker network connect [NETWORK] [CONTAINER]`  		  | 	Connects a container to a network
`docker network disconnect [NETWORK] [CONTAINER]`  	  | 	Disconnect a container from a network

## Information Commands

Command 									                | 	Info
---------------------------------------		| 	---------------------------------------
`docker logs [CONTAINER]` 					      | 	List the logs from a running container
`docker inspect [OBJECT_NAME/ID]`  			  | 	List low-level information on Docker objects
`docker port [CONTAINER]`  			          | 	Show port (or specific) mapping for a container
`docker top [CONTAINER]`  			          | 	Show running processes in a container
`docker stats [CONTAINER]`  			        | 	Show live resource usage statistics of containers
`docker system df`  			                | 	Check docker daemon disk space usage
`docker history [IMAGE]`  			          | 	Show the history of an image

## Other Commands

Command 									                  | 	Info
------------------------------------------  | 	---------------------------------------
`docker exec -it <container name> /bin/sh`  | 	SSH into container

