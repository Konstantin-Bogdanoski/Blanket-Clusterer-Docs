# Docker

Blanket Clusterer is available
on [hub.docker.com](https://hub.docker.com/repository/docker/kbogdanoski/blanket-clusterer), and it is ready for use.

The idea behind using a docker container was to provide the easiest way to scientists to use Blanket Clusterer without
configuring the different modules manually.

## Setup

### Install Docker

Before using the container, you must install docker on your machine. If you haven't installed it yet, refer
to [docs.docker.com](https://docs.docker.com/get-docker/) for installation steps.

After successfully installing and starting docker on your machine, log into your docker account.

After successfully logging to docker, open your preferred terminal, and simply use the following command:

```shell
docker pull kbogdanoski/blanket-clusterer:latest
```

This command will download the latest image of Blanket Clusterer from dockerhub, which is already setup with all the
necessary requirements for it to work.

After downloading the image, Blanket Clusterer is ready for use. Simply start the container using the following command:

```shell
docker run -it -p 80:80 -p 5000:5000 kbogdanoski/blanket-clusterer:latest
```

You might notice there are a couple of flags which we use. `-p 80:80` and `-p 5000:5000` are used to expose the ports
from which we will access the container.

`80:80` is needed for the GUI of the application, while `5000:5000` is needed for the `python flask`
backend application.



