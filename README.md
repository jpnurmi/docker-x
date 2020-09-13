# Docker X

A simple and generic Docker image primarily meant for building Yocto
images. Follow the instructions below to conveniently bind mount your
home directory into a Docker X container.

Notice that Docker X by itself does not build anything. It's purely
meant for conveniently switching to an environment that can be used to
build any project anywhere in your home tree.

## Build

    $ docker build -t docker-x --build-arg USER=$USER .

## Setup

    $ echo "alias docker-x='docker run --rm -ti -h docker-x -v $HOME:$HOME docker-x'" >> ~/.bashrc

## Run

    $ docker-x
