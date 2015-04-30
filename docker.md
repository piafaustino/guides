# Docker

> Docker is an open platform for developers and sysadmins to build, ship, and run distributed applications. Consisting of Docker Engine, a portable, lightweight runtime and packaging tool, and Docker Hub, a cloud service for sharing applications and automating workflows, Docker enables apps to be quickly assembled from components and eliminates the friction between development, QA, and production environments. As a result, IT can ship faster and run the same app, unchanged, on laptops, data center VMs, and any cloud.

https://www.docker.com/whatisdocker/

It's not a concrete description but that's the essence of Docker. It basically allows you to package and distribute your dev/deploy environments into images w/c you use as base for running your applications. 

## Engine

The Docker Engine is the executable you download and install when setting up Docker. It has 2 "modes": daemon (server) and client. You run the executable as a daemonized server for the machines you want to use Docker on. Then you send commands to the server using the same executable. Communication happens through unix sockets or via the HTTP API.

### Server

You run the Docker Engine in daemon (server) mode using the `-d` argument:

```
$ docker -d
```

Docker will be automatically run as a service if installed using most Linux distro package managers (e.g. apt-get, yum). 

TODO: Add details about configuring the server

### Client

You send commands to the Docker daemon using the same executable. For example, to build an image, you run `docker build .`. To run a container you run `docker run some_image`.

### Image

A Docker image is a "saved state" of an environment. An image is built using instructions from a `Dockerfile` and other arbitrary files you want to put in it. Images are stored and queryable from Docker registries. The Docker Hub is an example of a production installation of a registry. After building images you push them to a registry. You pull images from the registry to make them available inside the current machine.

TODO: Write about building images

### Dockerfile

The Dockerfile is a plaintext file containing instructions on how to build your Docker images. Here's an example:

```
FROM python:2.7
COPY . /usr/src/app
CMD ["python", "app.py"]
```

The first word in a line is your instructions followed by the argument of the instruction.

#### `FROM <image_name>`

The FROM commands allows you to extend an existing image. In the example above, we're extending the `python:2.7` image.

#### `COPY <LOCAL_PATH> <IMAGE_PATH>`

COPY copies files into the image. Note that LOCAL_PATH should be within your context. Your context is, by default, the current directory.

TODO: More commands

### Containers

Images themselves don't run your applications. You need to create containers where your applications will actually run. You can think of them as lightweight virtual machines. Though instead of virtualizing hardware and the OS of a system, your processes run on the same kernel as the host OS. If you're familiar with the concept of chroot or jailing then that's basically it plus some other features.

To create containers, run:

```
$ docker create image_name
```

This will output a container ID which you can use to reference the container when give commands to it. You can also give your own name for the container:

```
$ docker create --name some_name image_name
```

Start containers using the "start" command:

```
$ docker start some_name
```

You can combile these two steps using the "run" command:

```
$ docker run --name some_name image_name
```

TODO: More container commands

### Registry

## Machine

## Compose

## Swarm

## Local development

## Production deployment

## Best practices
