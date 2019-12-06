# Motorized_Focus_Camera
## Lets see how to test the Motorized Focus Camera Hardware from Arducam
 Arducam has released three demo function to test the Motorized focus camera, they are  Motorized_Focus_Camera_Preview.py, Motorized_Focus_Camera_Snapshot.py and Autofocus.py 
  - Before running this demo, you have to install Python Dependency libraries.
 ```Bash
 sudo apt-get install python-opencv 
 ```
 - Enable the I2C0 adapter by running below commands
 ```Bash
 chmod +x enable_i2c_vc.sh
 ```
 ```Bash
 ./enable_i2c_vc.sh
 ```
 -Then click 'y' to allow it reboot.
### Motorized_Focus_Camera_Preview.py
 - This demo supports focusing in preview mode, You can see the focus visually
 - Single focus by keyboard up and down
 - Run this demo by typing "sudo python Motorized_Focus_Camera_Preview.py" in the terminal.
### Motorized_Focus_Camera_snapshot.py
 - This demo supports focusing and save the image to the local filesystem. You can save the image after each focus.
 - Single focus by keyboard up and down
 - Run this demo by typing "sudo python Motorized_Focus_Camera_snapshot.py" in the terminal.
### Autofocus.py 
 - This demo supports auto focusing in preview mode, You can see the focus visually
 - Run the demo by typing "sudo python Autofocus.py" in the terminal.
### How to take a still using raspsitill command and store it locally 
```Bash
 - raspistill -o firstimage.jpg
``` 
### How to take a video using raspsitill command and store it locally 
This command will save a 5 second video file locally. Note default video time is 5 sec, which can be varied using -t 
```Bash
 - raspivid -o vid.h264
 ```
### MP4 Video Format
The Pi captures video as a raw H264 video stream. Many media players will refuse to play it, or play it at an incorrect speed, unless it is "wrapped" in a suitable container format like MP4. The easiest way to obtain an MP4 file from the raspivid command is using MP4Box.
Install MP4Box with this command:
```Bash
sudo apt install -y gpac
```
Then wrap MP4 around your existing raspivid output, like this:
```Bash
MP4Box -add vid.h264 vid.mp4
```
Alternatively, capture your raw video with raspivid and wrap it in an MP4 container like this:
```Bash
# Capture 30 seconds of raw video at 640x480 and 150kB/s bit rate into a pivideo.h264 file:
raspivid -t 30000 -w 640 -h 480 -fps 25 -b 1200000 -p 0,0,640,480 -o pivideo.h264 
# Wrap the raw video with an MP4 container: 
MP4Box -add pivideo.h264 pivideo.mp4
# Remove the source raw file, leaving the remaining pivideo.mp4 file to play
rm pivideo.h264
```

