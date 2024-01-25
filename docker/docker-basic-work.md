# Create a Dockerfile

# Build an Image from Dockerfile
`docker build -t welcome-to-docker .`
- `-t`: name tag of a future Image
- `.` is the path, that lets docker know, where it can find a dockerfile

# Create a containter, by running Image





# Commands
## Image
- `docker build -t IMAGENAME .`: builds an image
  - also can be written as `docker image build -t IMAGENAME .`
- `docker history [OPTIONS] IMAGENAME`: To see a history of an image
- `docker image inspect [OPTIONS] IMAGENAME`: displays detailed imformation on one or more images
- `docker image ls`: List images
## Container
- `docker container`: manages docker containers
- `docker container exec CONTAINER COMMAND`: executes a command on a container
- `docker container kill`: Kill container
- `docker container run`: Create and run a container from an Image
