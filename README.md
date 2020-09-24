# pi-security-camera

Enable camera in Interfaces
```
sudo raspi-config
```

Install motion
```
sudo apt-get install motion
```

Copy our config
```
sudo cp motion.conf /etc/motion/motion.conf
```

Start daemon
```
sudo nano /etc/default/motion
start_motion_daemon=yes
```

Turn off LED
```
sudo nano /boot/config.txt
disable_camera_led=1
```

Start the service
```
sudo service motion start
```

Reboot
```
sudo reboot
```
