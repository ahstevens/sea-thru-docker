# Sea-Thru Docker Container
Dockerized Implementation of Sea-thru by Derya Akkaynak and Tali Treibitz

__Forked from https://github.com/JQuezada0/sea-thru__

## Prerequisites

[Docker](https://docs.docker.com/get-docker/)

## Setup

1. Open a command line terminal and navigate to the project folder.
2. Build the container (may take some time): `docker compose up --build -d` 
3. Place source files in the root project directory; this directory gets mounted to `/opt/app/` in the container.
4. Enter the container via bash shell:  `docker exec -it seathru /bin/bash`
5. Run `python seathru.py --image ${PATH_TO_RAW_IMAGE} --depth-map ${PATH_TO_DEPTH_MAP}`
