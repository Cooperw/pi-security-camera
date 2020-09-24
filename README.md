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

Start the service
```
sudo service motion start
```
