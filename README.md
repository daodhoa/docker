Thank for your readme template:
https://gist.githubusercontent.com/PurpleBooth/109311bb0361f32d87a2/raw/8254b53ab8dcb18afc64287aaddd9e5b6059f880/README-Template.md
# docker
### Note: What your system downloaded: IMAGE, what your system run: CONTAINER

#### Docker image
```
docker image pull alpine
```
The ```pull``` command: fetches the images from Docker registry (Docker hub) and save it to your system
```
docker image ls
```
List all images in your system
```
docker container run alpine ls -l
```
when call ```run```, Docker client finds the image, create container and run command in that container. After the command finished, the container shut down

![alt text](https://training.play-with-docker.com/images/ops-basics-run-details.svg)
```
docker run alpine echo "Hello from alpine"
```
You should get the following output ```Hello from alpine```. In this case, docker ran the ```echo``` inside our alpine container and then exited. It happened very quickly.
Docker has a facility for iteracting with container shell by adding a flag to run container with an interactive terminal:
```
docker run -it alpine /bin/sh
```
To start exited container: ```docker start container_id```
