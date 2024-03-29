# Sea-Thru Docker Container
Dockerized Implementation of Sea-thru by Derya Akkaynak and Tali Treibitz

__Forked from https://github.com/JQuezada0/sea-thru__

## Prerequisites

[Docker](https://docs.docker.com/get-docker/)

## Setup

1. Open a command line terminal and navigate to the project folder.
2. Build the container (may take some time): `docker compose up --build -d` 
3. Enter the container via bash shell:  `docker exec -it seathru /bin/bash`
    - Replace `seathru` in that command if you've modified the `SERVICE` environment variable in `.env`
4. Place source files in the root project directory; this directory gets mounted to `/opt/app/` in the container.
5. Run `python seathru.py --image ${PATH_TO_RAW_IMAGE} --depth-map ${PATH_TO_DEPTH_MAP}`
    - This root directory is mounted into the container each time you bring it up via `docker compose up`, meaning any files you add on your host machine to this directory will _also_ be available within the container.
