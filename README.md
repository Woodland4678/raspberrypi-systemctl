# Raspi-systemctl for raspberry pi GRIP and mjpg-streamer

Runs raspberrypi camera on 1180, and usb camera on 1181. The mjpg-streamer-web runs independent of GRIP, and mjpg-streamer depends on GRIP. To use a USB camera instead of the raspberrypi camera, modify /etc/default/mjpg-streamer with the appropriate settings from /etc/default/mjpg-streamer-usb

Instructions based on https://github.com/WPIRoboticsProjects/GRIP/wiki/Running-GRIP-on-a-Raspberry-Pi-2.

1. Build/install mjpg-streamer - https://github.com/WPIRoboticsProjects/GRIP/wiki/Running-GRIP-on-a-Raspberry-Pi-2#installing-mjpg-streamer
2. Install Java
3. Install GRIP (>=1.3.0)
4. `sudo cp ./system/* /etc/systemd/system/`
5. `sudo cp ./default/* /etc/default`
6. `sudo systemctl enable grip`
7. `sudo systemctl enable mjpg-streamer`
8. `sudo systemctl enable mjpg-streamer-web`
