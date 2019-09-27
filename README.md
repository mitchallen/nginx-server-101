# nginx-server-101
--

## Usage

### Build

```
docker build -t mitchallen/nginx-server .
```

This example runs the server locally on port 1280.

    docker run -p 1280:80 --name nginx-server mitchallen/nginx-server


* * *

### Rerun with the same or a new container

```
docker stop nginx-server
docker rm nginx-server
docker run -p 1280:80 --name nginx-server mitchallen/nginx-server
```

* * *

### Confirm image is running

    docker ps
    
* * *


### Running Multiple Containers

You can run multiple containers on multiple ports like this:

```
docker run -p 1281:80 --name nginx1 mitchallen/nginx-server

docker run -p 1282:80 --name nginx2 mitchallen/nginx-server
``` 

Each server should have a unique set of values.

* * *

### Start and stop a running container

    docker stop nginx-server
    docker stop nginx1
    docker stop nginx2

    docker start nginx-server
    docker start nginx1
    docker start nginx2
    
* * *

### Remove

#### Remove Container

    docker stop nginx-server
    docker rm rnginx-server

### Remove Image

    docker stop nginx-server
    docker rm nginx-server
    docker rmi mitchallen/nginx-server

* * *