# Container Management

## List Containers

To list Docker containers, I used this command:

```bash
docker ps
```

No containers were present initially.

## Pull Latest Ubuntu Image

I pulled the latest Ubuntu image from Docker Hub using:

```bash
docker pull ubuntu
```

This downloaded the ubuntu:latest image.

## Run Container

I started a new container from the ubuntu image in detached mode with:

```bash
docker run -dit --name ubuntu ubuntu
```

This launched a container with `ID 0ebce5667046` in the background.

Checking again with `docker ps`:

```bash
CONTAINER ID   IMAGE     COMMAND   CREATED              STATUS              PORTS     NAMES
0ebce5667046   ubuntu    "bash"    About a minute ago   Up About a minute             ubuntu
```

## Remove Image

To remove the ubuntu image, I used:

```bash
docker rmi ubuntu
```

This failed with the error:

```bash
Error response from daemon: conflict: unable to remove repository reference "ubuntu" (must force) - container 0ebce5667046 is using its referenced image 457e4fa7416c
```

To solve it I first have to stop and remove the container before being able to remove the image.
