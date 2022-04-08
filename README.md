## Hardware Conncetion
![Alt text](https://github.com/ArduCAM/PTZ-Camera-Controller/blob/master/data/HardwareConnection.png)


## install opencv
* python3 -m pip install opencv-python
* sudo apt-get install libatlas-base-dev
* python3 -m pip install -U numpy 


## Download the source code 
```bash
git clone https://github.com/ArduCAM/PTZ-Camera-Controller.git
```

## Install libcamera
* cd PTZ-Camera-Controller
* python3 -m pip install ./libcamera-1.0.2-cp39-cp39-linux_armv7l.whl

## Add camera
* Edit the configuration file: sudo nano /boot/config.txt
* Find the line: camera_auto_detect=1, update it to:camera_auto_detect=0
* imx219 camera added: dtoverlay=imx219
* imx477 camera added: dtoverlay=imx477
* Save and reboot

## Enable i2c
* cd PTZ-Camera-Controller
* sudo chmod +x enable_i2c_vc.sh
* ./enable_i2c_vc.sh
Press Y to reboot



## Run the FocuserExample.py

cd PTZ-Camera-Controller
python3 FocuserExample.py


![Alt text](https://github.com/ArduCAM/PTZ-Camera-Controller/blob/master/data/Arducam%20Controller.png)



## Refering the link to get more information about the PTZ-Camera-Controller
http://www.arducam.com/docs/cameras-for-raspberry-pi/ptz-camera/