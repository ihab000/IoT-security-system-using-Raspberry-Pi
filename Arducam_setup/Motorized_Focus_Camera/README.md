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
