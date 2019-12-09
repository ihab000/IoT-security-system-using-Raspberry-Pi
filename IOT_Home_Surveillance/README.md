                                                 # IOT Home_Surveillance
   To build a security system that runs on Raspberry Pi to detect the motion and capture the picture of the person and send image notification to my dropbox API. 


## Directory Structure
    |__IOT_Home_Surveillance              # IOT Home Surveillance Project directory
       |__ pi_surveillance.py             # Main program to run
       |__ conf.json                      # Java configuration file
       |__ pyimagesearch    
          |__ __init__.py
          |__ tempimage.py
       |__README.md

### Prerequisites
### Hardware Requirements
* [Raspberry Pi 3 Model B+ Basic Kit](https://www.canakit.com/raspberry-pi-3-model-b-plus-basic-kit.html)
* [Arducam Auto Focus Pi Camera,Motorized Focus Lens, OV5647 5MP 1080p](https://www.amazon.com/Arducam-Autofocus-Raspberry-Motorized-Software/dp/B07SN8GYGD/ref=pd_sbs_147_t_1/143-5613826-8442854?_encoding=UTF8&pd_rd_i=B07SN8GYGD&pd_rd_r=7fa37d1b-53a0-4005-809f-3665b7b6f359&pd_rd_w=M7jVH&pd_rd_wg=hePs6&pf_rd_p=5cfcfe89-300f-47d2-b1ad-a4e27203a02a&pf_rd_r=WZM83MDYYVAS985JE5XY&psc=1&refRID=WZM83MDYYVAS985JE5XY)

### Software Requirements
* [Python](https://www.python.org/)
* [OpenCV](https://opencv.org/)
* [Dropbox](https://www.dropbox.com/developers)

Please run the below command to install all the required packages
```
pip install -r requirements.txt
```
### Dropbox Setup
* Follow the link given for dropbox above, then sign in with your gmail account and create an app like below
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/Dropbox_app.png)
* Generate your API key and input it in conf.json file
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/generate_API.png)

### Running the tests
Please run the below command to run the surveillance camera
```
python pi_surveillance.py --conf conf.json
```
### Results
The security surveillance video streams all the time with unoccupied status and when a person moves in the room, then opencv helps to detect the person and the staus changes to "occupied" and an image of particular frame with the person will be sent to the dropbox account linked.
* Below picture is when I was in the room
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/OccupiedStatus.png)
* Created App in the dropbox has the received images
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/3_upload_dropbox.png)
* Teminal updates
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/3_upload_terminal.png)
* Dropbox home looks this way
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/dropbox_home.png)
