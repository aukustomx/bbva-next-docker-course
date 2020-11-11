##Content
1. Installation on Linux
1. Overview Docker vocabulary
    1. Docker Engine
    1. Docker Image
    1. Docker Container
    1. Docker Registry
    1. Dockerfile
    1. Orchestration
1. Running a container
1. Container features
    1. Layers
    1. Ephemeral
    1. Container vs VMs
1. Images
    1. Listing images
    1. Pulling images
    1. More on layers
    1. Building images
    1. Dockerfile
        1. Dockerfile instructions
        1. Layers
        1. Building an image
        1. Tags
1. Running my container
    1. Enter my container 
    1. Volumes
1. Advanced
    1. Volumes
    2. Networking
    3. Compose
    4. Swarm
    5. Kubernetes
1. Final exam

##Installation on Linux
To install Docker on you OS, please visit [Get Docker](https://docs.docker.com/get-docker/). 

We are going to install Docker using official Docker repository. In this case we will install it on Debian.
```shell script
sudo apt-get remove docker docker-engine docker.io containerd runc

sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io
```
Verify that Docker is installed correctly by running the following command:
```shell script
sudo docker run hello-world
```
By default Docker runs only as root user. If you would like to use Docker as a non-root user, you must add your user to the “docker” group with something like:
```shell script
sudo usermod -aG docker $USER
```
You need to log out and back in for this to take effect.
    
