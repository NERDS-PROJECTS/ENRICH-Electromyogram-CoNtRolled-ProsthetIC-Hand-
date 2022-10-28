# ENRICH-Electromyogram-CoNtRolled-ProsthetIC-Hand
 Description of the technology
 
Electromyogram (EMG) signal classification to detect various upper-limb movements have been used for many applications, including hand prosthesis control for last two decades. Prosthetic hand control has fired the imagination of many researchers and thousands of papers have been published in the field, but the user acceptance has not been strong and there appears to be a significant gap between the published research and its translation [1]. Some notable researchers have reported the classification of grasp modes using different number of EMG signal channels to generate accurate recognition rate of different types of grasping. Almost all literature reports focus on the classification of EMG signals and their application for controlling finger movements in robotic hand, not for robotic hand grasping operations. 
ENRICH has response time of 250 milliseconds which is comparable to human hand response time (~300 milliseconds). The control of the hand ENRICH is shown in Figure 1. The EMG signal generated from the muscle is acquired using single channel Ag/AgCl surface EMG electrodes. The signal is amplified and faded to the controller. The controller then pre-processes the signal and grasping features is extracted. The control signal based on the feature is given to the actuators.  That is how the prosthetic hand grasp an object. 

![image](https://user-images.githubusercontent.com/99505309/198611328-ed22ff28-3303-4162-8958-d978c5bc9a21.png)


Figure 1:  Block Diagram for control of ENRICH.

The design and development of a data logger wherein a continuous signal from a source is fed to circuit and circuit stores input data into its memory as well as upload it to a server. Initially data from a signal generator is saved using Coolterm software. It is a system dependent method, where an Arduino needs to be connected to a computer for saving the data. To make it stand alone system, a datalogger circuit is developed. Figure 2 shows the working of the data logger. ESP32 and ESP8266 module were considered for datalogging system. It contains the Wi-Fi-module, thereby directly uploading the data to the spreadsheet in google. Furthermore, another key aspect was to save the data in a physical device or a memory. For this, SD card module was added in the circuit. The ESP32 connects the circuit to the internet using a particular IP address with user’s access name and password of Wi-Fi connectivity.


![image](https://user-images.githubusercontent.com/99505309/198612911-16b91847-ef95-45b0-90d5-985caf3dbeeb.png)



Figure 2:  Block Diagram of working of the data logger    


![image](https://user-images.githubusercontent.com/99505309/198610921-730f2f8a-6324-4f98-b8f5-dea4609d3410.png)
 
Figure 3: Circuit diagram for datalogger
We are using a ESP32 module with SD card module (as shown in Figure 3) to save the signal generator data in the SD card. Previously, the signal generator data was saved in google spreadsheet. Appscript software is used while connecting with the Wi-Fi username and password and auto updating the real-time data in the spreadsheet using the Arduino IDE code. 
 
