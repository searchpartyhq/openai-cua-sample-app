## Overview

We want to build a _dockerized_ version of the CUA

```shell
# Build the Docker file in our repo
docker build -t cua-sample-app .
# Run the container
docker run --rm -it --name cua-sample-app -p 5900:5900 -e DISPLAY=:99 cua-sample-app

# then run 
uv run python simple_cua_docker_loop.py
```