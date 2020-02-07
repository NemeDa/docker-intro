# Setup A Mqtt Server

with docker-compose (*work in progress*)

---
<!-- .slide: class="left" -->
### Step 1- Install Compose / Setup MQTT CLient

Follow: <https://docs.docker.com/compose/install/>
and <https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-the-mosquitto-mqtt-messaging-broker-on-debian-9>

Note: TBD improve slide

---
<!-- .slide: class="left" -->
### A docker-compose.yml file example

```dockerfile
<!--#include file="src/docker-compose.yml" -->
```

---
<!-- .slide: class="left" -->
### Setup Environment Variables on Linux

1. ssh to your docker-toolbox (IP is most of the time something like 192.168.99.100)
2. edit/create `/etc/environment`:

    ```bash
    sudo vi /etc/environment
    ```

3. and add the following line:

    ```bash
    USERDIR="/home/docker"
    ```

4. sadly, we have to restart docker-toolbox (so do that)

---
<!-- .slide: class="left" -->
### Setup Network Bridge for Mqtt (VS Code)

1. switch to Docker sideboard
2. click `+` (create) on Network "Box"
3. choose Bridge and name it `mqtt`
