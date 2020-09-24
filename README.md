# pi-security-camera

Origional Instructions found here: https://www.instructables.com/id/Raspberry-Pi-Motion-Detection-Security-Camera/

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

On your main computer (linux, mac, or windows subsystem), add this to your .bashrc to pull and clean captures
It will need to be modified to fit your stuff, ssh-keys are used for authentication
```
alias cameras='for x in $(cat hosts); do scp -r pi@$x:/var/lib/motion/* /mnt/c/Users/Cooper/Downloads/motion/;echo "sudo rm /var/lib/motion/*" | ssh pi@$x; done'
```

Modify and save a bookmark for the html files to get livestreams
