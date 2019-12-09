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
### Running the tests
Please run the below command to run the surveillance camera
```
python pi_surveillance.py --conf conf.json
```
### Results
The security surveillance video will be running all the time and When a person moves in the room, the it detects the person moving send an image frame to the dropbox linked.
![alt text](https://github.com/sooryanivedhaashokan/IoT-security-system-using-Raspberry-Pi/blob/master/IOT_Home_Surveillance/result_snapshots/OccupiedStatus.png)
