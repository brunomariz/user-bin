# user-bin

Linux user scripts and executables


### tempc

##### Installation

1. Download the script
2. Change their permissions so they're executable

```shell
chmod 744 tempc
```

3. Move it to the ~/bin directory

```shell
mv tempc ~/bin/tempc
```

4. Add ~/bin to $PATH if it is not already added

Add this line to the end of ~/.bashrc file

```bash
export PATH="$HOME/bin:$PATH
```

##### Script usage

```
Run a temporary container.
Default command run by script: docker run --rm -it DOCKER_IMAGE /bin/bash

Syntax: tempc [-h|n:|p:|s|v] [-- OTHER_DOCKER_ARGUMENTS] DOCKER_IMAGE
Example: tempc -n server -- --net my-net --ip 172.18.50.50 ubuntu
options:
h       Print this Help.
n NAME  Set container name and hostname.
p PORT  Set shared ports. PORT should be in the same format as docker -p argument, HOST_PORT:CONTAINER_PORT
s       Create shared volume at $PWD:/home/$USER/shared.
v       Print software version.
x       Share GUI display. Pair with 's' option to save graphical application files on host.
```


