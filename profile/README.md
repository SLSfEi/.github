# SLSfEi : Smart LIDAR System for Explosives Installation
SLSfEi is a system to facilitate explosive installation processes in the mining industry. With rplidar device, the system can provide the operator with real time position data for accurate explosive installation. Which can reduce the error and cost of this operation. The operator can easily interface with the system using a web browser on their smartphone or computer.

# System diagram
![system diagram](./profile/SLSfEI.drawio.png)

The system has 2 parts.
- [Web Application](https://github.com/SLSfEi/web-app) that the operator can interface with.
- [Scan Provider](https://github.com/SLSfEi/scan-provider-cpp) that process data from rplidar device.

Both parts are then combined into a single [docker container](https://github.com/SLSfEi/docker-stack) for ease of deployment.

**Note:** Further details about each part are provided in their respective repositories.

# Hardwares
The system is intended to be deploy on `raspberry pi 4` and `slamtec rplidar a1m8`.

`raspberry pi 4` will have following programs installed:
- `docker` and `docker-compose` to run containerized version of the system.
- [`raspap-webgui`](https://github.com/RaspAP/raspap-webgui) to make wifi AP for portable access.

`slamtec rplidar a1m8` will be connected to `raspberry pi 4` via a USB cable.
