# ESP32-CAM: remoted object detection camera #

## Demonstration
https://www.youtube.com/watch?v=4a_r6fCYZ3U

## Descrition

The ESP32-CAM would stream the images to PC via TCP packages, then the remote software in PC would receive the images and do the object detection with Tensorflow Lite(SSD Mobilenetv2) or Keras (YOLOv3).

### Hardware setup
Components are used: ESP32-CAM module, RC Servo x2, 5V Battery.<br/>

### Software setup
The software contains 2 parts<br/>
1. ESP32-CAM firmware<br/>
- Use Arduino IDE to flash firmware to ESP32-CAM module.<br/>
2. Remote control software (Can be run on Ubuntu or Windows PC)<br/>
- ubuntu: Install virtualenv<br/>
```bash
sudo apt-get install python3-pip
sudo pip3 install virtualenv
cd ESP32CamObjectDetection/remote
virtualenv -p python3 <env_name>
source <env_name>/bin/activate
(<env_name>)$ pip install -r requirementVirtualenv.txt
```
- windows 10: Not yet checked but it should be similar<br/>
Run remote control:<br/>
```bash
python3 main.py
```
Note: If your computer does not have GPU, update setting.ini by changing GPU = 0, or you can change like this to run the code in CPU
