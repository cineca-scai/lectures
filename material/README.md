
# Python, notebooks, objects and MapReduce

This is a [CINECA](http://www.cineca.it/) training event.

A read-only version of our notebooks can be accessed with
[nbviewer](http://nbviewer.jupyter.org/github/cineca-scai/lectures/tree/sns/material/) free service reading the GitHub repository.

## Prerequisites

* docker 1.13+

To install docker on a unix terminal, you can:

```
# Install docker
curl -sSL https://get.docker.com/ | sh
```

For Mac and Windows user the best way to get Docker tools working,
is using their new [toolbox](https://www.docker.com/toolbox).

## How to use lectures interactively

On a terminal, launch the docker image:

```
docker run -d \
    --name mynotebook \
    -e LECTURE_BRANCH=sns \
    -e LECTURE_PATH=material \
    -h mynotebook \
    -v cineca_spark_volume:/data/lectures \
    -p 80:8888 \
    pdonorio/jupy36:alpine

## Other operations:

# To freeze the container
docker stop mynotebook
# To remove the frozen container
docker rm mynotebook
```

### Access the web jupyter notebooks pages

Visit with your browser the jupyter running server at:

[http://localhost](http://localhost).

<small>Note: if you use docker on Mac or Windows, instead of *localhost* you
should find the virtual machine IP where Docker is running.
This is usually possible with commands like `boot2docker ip` or `docker-machine ip`.</small>
