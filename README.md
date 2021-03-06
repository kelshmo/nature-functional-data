# nature-functional-data
Processing code for CommonMind Consortium Nature scientific data paper SDATA-19-00213B.`kelshmo/covarr` Docker available with required compute dependencies. 

## Install Docker 

1. [Find your supported platform and download Docker.](https://docs.docker.com/v17.12/install/#supported-platforms)

## Run Container

This Docker container is built on [`rocker/tidyverse`](https://hub.docker.com/r/rocker/tidyverse/) producing a debian stable work environment. 

1. To get container for the first time: `docker pull kelshmo/covarr`
2. Suggested configuration for running container: 
```
docker run -d -p 8787:8787 -e PASSWORD=<insert password> kelshmo/covarr #replace <password> with your password
```
- `-d` flag allows you the retain use of the terminal while the Docker image is running 
- `-p` specifies port of choice
- `-e` designates a password to login to RStudio

If you are having trouble with your Docker, this [documentation](https://ropenscilabs.github.io/r-docker-tutorial/02-Launching-Docker.html) (or [this documentation](https://github.com/rocker-org/rocker/wiki/Using-the-RStudio-image)) may be useful.

3. Now, RStudio has launched invisibly. Open a browser and enter your ip address followed by :8787. You should be greeted by the RStudio welcome screen.

username: rstudio
password: <password>
  
4. You can `docker stop <container name>` to pause your work and return to it later with `docker start <container name>`.

* To find your container name `docker ps -a`

## Access to Data 

Data access requires a [Synapse account](https://docs.synapse.org/articles/getting_started.html) and access to the [CommondMind Consortium Knowledge Portal](https://www.synapse.org/#!Synapse:syn2759792/wiki/69613).   
