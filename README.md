# docker_elasticsearch

# Installation

Download base image.

```sh
$ docker build -t="dockerfile/ubuntu" github.com/dockerfile/ubuntu
$ docker build -t="dockerfile/java" github.com/dockerfile/java
```
Bilud image

```sh
$ docker build docker build -t YOUR_IMAGE_NAME .
```

Run image

```sh
$ docker run -d -p 9200:9200 -p 9300:9300 YOUR_IMAGE_NAME
```

You may need to configure port forward settings to access docker container on virtual machines.

```sh
$ VBoxManage controlvm "boot2docker-vm" natpf1 "elasticsearch,tcp,127.0.0.1,9200,,9200"
```

Delete port forward settings.

```sh
$ VBoxManage controlvm "boot2docker-vm" natpf1 delete elasticsearch
```
