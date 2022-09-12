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
* (Optional) Configure mDNS to add a custom hostname
    * `sudo apt install avahi-daemon`
    * Enable the host and domain properties in `/etc/avahi/avahi.conf`
