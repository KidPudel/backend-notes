# Create a Dockerfile
```Dockerfile
# Start Image from a base Image ( You can find base images in Docker Hub)
FROM node:18-alpline

# Image is it's own space, so it has a file system
# We can set our current working directory
WORKDIR ./app

# Now to copy the application into the image, we use COPY
# Here we are saying: "Copy files in current project directory, into a certain directory in that image
COPY . ./


# Copy other stuff in other image directories
# ⬇️ in image it's ./app/src, you got it
COPY ./src ./src 
COPY ./ignore ./ignore

# Now to install, configure and build, and clear
RUN npm install \
    && npm install -g serve \
    && npm run build \
    && rm -fr node_modules

# Start the app
CMD [ "serve", "-s", "build" ]

```

Or simpler version

```Dockerfile
# Start on base image
FROM node:18-alpine

# Copy our program to run to the image's directory
COPY . ./app

# Now to execute we run a vanilla command
CMD node run ./app/main.js

# Alternatively, we can navigate to the ./app directory, by switching working directory (like cd (current working directory)
WORKDIR ./app
CMD node run main.js
```

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
