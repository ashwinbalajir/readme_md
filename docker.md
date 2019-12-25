- Create docker file for express app (DockerFile)
- Add below config

```
FROM node:10

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

EXPOSE 3000
CMD [ "node", "index.js" ]

```
- Create .dockerignore file (Add files you dont want to push to image)

```
node_modules

```
# Commands to create and push image to container
```
 docker build -t <image name> .
 docker images (To check image)
 docker run -p 49160:8080 -d <image name> (8080- app running port; 49160 host os port )
```
Inside docker multiple application can run on same port, but host port should be different.
# Get container ID of running services
```
 docker ps  
```
# Print app output
```
 docker logs <container id>
```

# Enter the container
```
 docker exec -it <container id> /bin/bash
```

# To remove image and container

- Delete the container first.
- If container is running. stop the container first and then remove
```
 docker container stop <containerid>
 docker container rm <containerid>
 docker image rm <imageid or name>

 ```


 # For running build image and container through docker-compose

 ```
    version: '3'
    services:
    app:
        container_name: express-yaml-try
        restart: always
        build: .
        ports:
        - '80:3000'
```

# Command to run
```
 docker-compose up
 use -d flag to run in background

```
# To re-build
```
docker-compose build
```

