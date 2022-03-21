---
description: 🐋
---

# Docker

{% hint style="info" %}
If you want to run Docker natively in Windows, run `bcdedit /set hypervisorlaunchtype auto`in a privileged CMD. Note that you won't be able to run Virtual Machines with this configuration. To deactivate this feature, run `bcdedit /set hypervisorlaunchtype off`.
{% endhint %}

## Vulnhub

First of all, docker can help us to train against specific vulnerabilities deploying a vulnerable envirnoment in a blink of an eye. The list of pre-built environments based on Docker-Compose can be found [here](https://github.com/vulhub/vulhub).&#x20;

{% tabs %}
{% tab title="Installation" %}
```
# Install pip
curl -s https://bootstrap.pypa.io/get-pip.py | python3

# Install the latest version docker
curl -s https://get.docker.com/ | sh

# Run docker service
service docker start

# Install docker compose
pip install docker-compose
```
{% endtab %}

{% tab title="Usage" %}
```
# Download project
wget https://github.com/vulhub/vulhub/archive/master.zip -O vulhub-master.zip
unzip vulhub-master.zip
cd vulhub-master

# Enter the directory of vulnerability/environment
cd flask/ssti

# Compile environment
docker-compose build

# Run environment
docker-compose up -d

# After the test, delete the environment with the following command.
docker-compose down -v

# remove all unused containers
docker container prune
```
{% endtab %}
{% endtabs %}

## Docker for Pentest

There are several assessments, evaluations, tools and frameworks that are SO much easier to deploy using a container. I followed [this guide](https://blog.ropnop.com/docker-for-pentesters/), and I found of interest the following:

## Docker Cheat Sheet

{% tabs %}
{% tab title="Useful commands" %}
```
docker ps
docker inspect <container_name>
docker rmi -f <image_id>
```
{% endtab %}

{% tab title="TestSSL" %}
```
docker run -ti drwetter/testssl.sh <your_cmd_line>
```
{% endtab %}

{% tab title="NGrok + Nginx" %}
```
./ngrok authtoken token
./ngrok http 680

docker run --rm -it -p 680:80 -p 6443:443 -v "${PWD}:/srv/data" rflathers/nginxserve
```
{% endtab %}

{% tab title="OWTF" %}
```
docker build -t owtf <path to dockerfile directory>
docker run -it -p 8008:8008 -p 8009:8009 -p 8010:8010 owtf /bin/bash
docker run -it -p 8008:8008 -p 8009:8009 -p 8010:8010 nikitux/owtf /bin/bash
```
{% endtab %}

{% tab title="Metasploit" %}
```
metasploitports='docker run --rm -it -v "${HOME}/.msf4:/home/msf/.msf4" -p 8443-8500:8443-8500 metasploitframework/metasploit-framework ./msfconsole' 
```
{% endtab %}

{% tab title="MobSF" %}
```
# Install docker
sudo apt install docker.io -y

# Pull the image
sudo docker pull opensecurity/mobile-security-framework-mobsf:latest

# Deploy the container
sudo docker run --rm -it -p 8800:8800 opensecurity/mobile-security-framework-mobsf:latest
```
{% endtab %}

{% tab title="Mara" %}
```
docker run -it -v ${PWD}:/apps --rm xyphex/mara-framework
docker exec -ti [CONTAINER-ID] /bin/bash
```
{% endtab %}
{% endtabs %}
