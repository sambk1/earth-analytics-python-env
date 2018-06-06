# earth-analytics-environment
Welcome to the Earth Analytics Environment Repository! Here you will find a conda envt that can be installed on your computer using a ``.yml` file. You will also find a docker image that can be used to actually run the environment in a containerized environment.

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/earthlab/earth-analytics-binder/master)

## Contributors:

* Leah A. Wasser
* Chris Holdgraf
* Max Joseph
* Martha Morrissey

## Getting started with the Conda Environment

### 1. Install the Earth Lab Conda Environment on your Local Computer.

To begin, install the conda for Python 3.x. We suggest 3.6 now.
We recommend installing geo-related dependencies with `conda-forge`. We
have created a custom yaml list with all of the dependencies that you will
need to run the lessons in this course. Follow
these steps below to get your environment ready.

About Conda Environments: https://conda.io/docs/user-guide/tasks/manage-environments.html

An environment for conda has been created specifically for this course. To load this run:

`conda env create -f environment.yml`

* Note that it takes a bit of time to run this setup
* Also note that for the code above to work, you need to be in the directory where the `environment.yml` file lives.

To manage your conda environments, use the following commands:

#### View envs installed
`conda info --envs`

#### Activate the environment that you'd like to use

`source activate myenv-name`

In our case, the environment that we are using is called: `earth-analytics-python`. This name is
defined in the `environment.yml` file. Thus you'd type:

`source activate earth-analytics-python`

to activate it once it's installed.

## Docker Build

[![Docker Automated build](https://img.shields.io/docker/automated/earthlab/earth-analytics-python-env.svg)](https://hub.docker.com/r/earthlab/earth-analytics-python-env/)

[![Docker Build Status](https://img.shields.io/docker/build/earthlab/earth-analytics-python-env.svg)](https://hub.docker.com/r/earthlab/earth-analytics-python-env/)

To run a docker container you need to do the following:

1. [Install docker](https://docs.docker.com/install/) and make sure it is running.

2. Build the docker image on your compute locally. Be patient - this will take a bit of time.
Run the following lines to build the docker image locally:

```
cd earth-analytics-python-env
docker build -t earthlab/earth-analytics-python-env .
docker run -it -p 8888:8888 earthlab/earth-analytics

```

3. Run the image.

To run your earth-analytics image, use the following code:

`docker run -it -p 8888:8888 earthlab/earth-analytics-python-env`

NOTE: `earthlab/earth-analytics-python-env` is the name of this image as built above. To
view all images on your computer, type
`docker images --all`

One you run your image, you will be given a URL at the command line. Paste that puppy
into your browser to run jupyter with the earth analytics environment installed!!
