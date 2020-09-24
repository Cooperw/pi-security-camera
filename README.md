# pi-security-camera

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

Enable camera in Interface Options and then reboot
```
sudo raspi-config
```
