# user-bin

Linux user scripts and executables


### tempc
  
```
Run a temporary container.
Default command run by script: docker run --rm -it DOCKER_IMAGE /bin/bash

Syntax: tempc [-h|n:|p:|s|v] DOCKER_IMAGE
options:
h       Print this Help.
n NAME  Set container name and hostname.
n PORT  Set container name and hostname. PORT should be in the same format as docker -p argument, HOST_PORT:CONTAINER_PORT
s       Create shared volume at $PWD:/home/$USER/shared.
v       Print software version.
```


