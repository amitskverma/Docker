 history


    1  docker version
    2  docker container ls
    3  docker image ls    // list images
    4  docker images  // list images
    5  docker images ls -a  // not working become images and ls are both command
    6  docker run redis
    7  docker container ls
    8  docker container ls -a
    9  docker stop 41fe34ce56b3  // to stop specfied iD container
    10  docker container ls -a
    11  docker stop 878d25748992 
    12  docker stop bc9b6e2e7a8d
    13  docker stop bc9b6e2e7a8d 312b8006f983 
    14  docker stop 10bf4981b990
       docker stop -f $(docker ps)

    15  docker ps -a
    16  docker rm -f $(docker ps -aq)
    17  docker images
   
    18  docker image ls
    19  docker rmi ubuntu
    20  docker pull nginx:1.14-alphine
    21  docker pull nginx:1.14-alpine
    22  docker run -d --name webapp nginx:1.14-alpine
    23  docker ps -a
    24  docker rmi $(docker images)
    25  docker image
    26  docker images\\n
    27  docker rmi 8a2fb25a19f5\n
    28  docker rmi 8a2fb25a19f5 -f\n
    29  docker rmi -f  8a2fb25a19f5\n
    30  history
    31  docker stop d7e68c947e8d
    32  docker rmi -f  8a2fb25a19f5\n



docker run -p 38282:8080 --name blue-app -e APP_COLOR=blue -d simple-webapp
```

| Part | Flag | Meaning |
|------|------|---------|
| `docker run` | — | Create and start a new container |
| `-p 38282:8080` | `-p` | Map host port **38282** → container port **8080** |
| `--name blue-app` | `--name` | Name the container **blue-app** |
| `-e APP_COLOR=blue` | `-e` | Set environment variable `APP_COLOR` to `blue` inside the container |
| `-d` | `-d` | Run in **detached mode** (background, not blocking terminal) |
| `simple-webapp` | — | The **image** to create the container from |

**What happens when you run it:**
```
1. Docker pulls 'simple-webapp' image (if not found locally)
2. Creates a container named 'blue-app'
3. Sets APP_COLOR=blue inside the container
4. App starts and listens on port 8080 internally
5. You access it via → localhost:38282
