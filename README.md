# hass_setup
HASS Setup with Docker Compose

## Description

The idea is to run HASS using Docker Compose and have a MySQL/MariaDB instance with persistent storage.
The HASS setup and data must be kept between `docker compose up` and `docker compose down`.

HASS URL: `http://localhost:8123`

## Installing pre-requisites on Lubuntu

* Install the Docker Engine using the guide under: https://docs.docker.com/engine/install/ubuntu
    * Do not install the Docker Desktop app as it is not needed. Only the Docker Engine and Docker Compose are required.
* Install the Docker Compose script (it could have already been installed on the step above): `sudo apt install docker-compose-plugin`
* Create an SSH Key and add it to the SSHD in order to download the content of this repository.
    * /etc/ssh/ssh_config: Add XX
* Allow SSH connection from the local network.
    * /etc/ssh/sshd_config: Add XX
* Configura mDNS to add a custom hostname
    * `sudo apt install avahi-daemon`
    * Enable the host and domain properties in `/etc/avahi/avahi.conf`

## Display dashboard in a Google Cast
* Install `catt`: `pip3 install catt`
* Start casting: `catt -d "Office Display" cast_site http://hass.local:8123/google-cast/0`
* Stop casting: `catt -d "Office Display" stop`
