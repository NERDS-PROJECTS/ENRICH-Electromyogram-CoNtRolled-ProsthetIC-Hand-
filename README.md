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
 


Name of the Technology: ENRICH by Prof. Nayan M. Kakoty.
Patent Application Number: 201931049269.
Status: Published

Related Literature:
From grasping and manipulating objects to grooming and communication, the versatility of the human hand is integral to both physical survival and social conventions. The loss of one or more hands is, thus, a devastating experience, requiring significant psychological support and physical rehabilitation. 
Fajardo et al. [5], The strict development processes of commercial upper-limb prostheses and the complexity of research projects required for their development makes them expensive for end users, both in terms of acquisition and maintenance. Moreover, many of them possess complex ways to operate and interact with the subjects, influencing patients to not favour these devices and shed them from their activities of daily living. The advent of 3D printers allows for distributed open-source research projects that follow new design principles; these consider simplicity without neglecting performance in terms of grasping capabilities, power consumption and controllability. Its modular, parametric and self-contained design is intended to aid people with different trans radial amputation levels. This approach allows for easy updates of the system and demands a low cognitive effort from the user, satisfying a trade-off between functionality and low cost. 
Leobardo et al. [6], The use of a commercial EMG armband for the motion control of a prototype hand prosthesis is based on mechanical design of an open source six degree-of-freedom hand. The modification in actuation and power transmission devices to reduce the prototype's costs and to provide a major mobility to the thumb motion in adapting the different object grasp type. Unlike some similar prototypes previously reported and considering that the proposed application requirement of portability, the use of a PC for the acquisition and processing of the EMG data has been replaced by a portable hardware system based on the master/slave architecture. The master device is a Raspberry Pi-based subsystem interfaced with the EMG armlet for gathering and classifying information from the user's muscular activity. The slave device is an ATmega328 microcontroller-based subsystem that defines the movements of the robotic hand from the information collected and processed by the master device. 
Abarca et al. [7], This work describes the development of a prosthesis hand prototype with an active wrist. The Octa Hand can perform at least six grasping shapes: rest, tip, tripod, power, spherical and extension. Cables and pulley mechanism was used on each finger to enable the flexion/extension and under-actuated abduction/adduction movement while worm drive and internal helical gear mechanisms were used on the wrist to enable the flexion/extension and pronation/supination movements. To obtain an anthropomorphic, compact, low-weight and low-cost result, the prototype was designed based on a CAD model using 3D scanner technology, and the prototype was manufactured with 3D printed technology with a total weight of 950g.
Zhou et al. [8], The thumb of a natural hand or a prosthetic hand plays a significant role in realizing a hand's grasping and manipulation activities. This requires that mechanical design of a prosthetic hand should allow its thumb to perform both abduction/adduction and flexion/extension in order to mimic a natural hand's grasping and manipulation abilities with a minimum number of actuators. The thumb and the whole prosthetic hand were fabricated using a low-cost three-dimensional printing technology, with sizes comparable to those of real human ones but with much lighter weights. Based on the concepts of soft robotics and under actuation, the thumb shows significant mechanical compliance and performs well in power grasps, precision grasps, and lateral grasps of different shaped and sized household objects. The soft thumb has two modes of operation based on an innovative and compact mechanism, and one actuator only offers grasping versatility.
Atasoy et al. [9], The anatomical structure of the hand and its parts; muscles, tendons, bones, and ligaments give the hand its dexterous capabilities in a very efficient way. Studying these structures is important for adapting anthropomorphic features in prosthetic devices. Giving the anthropomorphic features to a prosthetic hand increases the complexity of the mechanical design; therefore, the control of the system can simplify the mechanical structure.


![Screenshot (197)](https://user-images.githubusercontent.com/99505309/201054337-598d83fb-a158-4ee4-ba17-1524e0e94e41.png)

MG958 [10] servo motor (shown in Figure 6) is use for high torque purpose ranging more than 15KG. Its operational range is from 4.8-6V and gives a full-scale movement of 180 degrees. Its response time is 0.18sec per degree when it is operated in 4.8V and 0.15sec degree operating in 6V.

 
 ![image](https://user-images.githubusercontent.com/99505309/198616656-48083993-fd6b-411b-94eb-d8aa88cc42c6.png)

Figure 6: MG958 servo motor

ESP32 [7] (shown in Figure 7) is a powerful, generic Wi-Fi+ BT+BLE MCU module that targets a wide variety of applications, ranging from low-power sensor networks to the most demanding tasks, such as voice encoding, music streaming and MP3 decoding.
An alternate for ESP32 is NODEMCU/ESP8266 [12] module having similar features of Wi-Fi connectivity and Bluetooth. In the setup the analog input is configured in order to exploit the whole range, the analog input is converted by a 12-bit ADC therefore the conversion result goes from 0 to 4095, with attenuation of 6dB the full scale corresponds to 2.2V. The Wi-Fi part of the card is then configured and the connection to the Wi-Fi network is made. The web server is then instantiated on the card and will respond to our http queries.  You instantiate a client object that waits for connections. When a connection is detected, the http request is read (in our case absolutely trivial) and the response is prepared. In our case the response is the reading of the acquired analog signal.

 
 ![image](https://user-images.githubusercontent.com/99505309/198616452-69fe4cdd-c23e-4a80-b269-62cb476aabe1.png)

Figure 7: ESP32


Relevant Patent:
Title: Electromyography with prosthetic or orthotic devices
Inventor: Árni Einarsson, Stefán Páll Sigurþórsson, Atli Örn Sverrisson
Application no: US11051957B2
Abstract: Systems, devices and methods for control of a prosthetic or orthotic device (POD) based on electromyography (EMG) signals are described. The POD may be a lower or upper limb POD having one or more joints. One or more EMG sensors may detect the EMG signals. The EMG sensors may be external, subcutaneous, intraperitoneal, epimysial, intramuscular, or other types. Control of the POD may be based on EMG and non-EMG signals, such as velocity, acceleration, position, force, etc. Voluntary and/or automatic control may be implemented, for example with voluntary muscle contractions and/or data based on velocity, acceleration, position, force, etc. In some embodiments, the neutral position of an ankle POD is adjusted based on EMG signals.

Problems that can be Solved by the Technology Developed and Solution Methodology:
In recent years, assistive devices have been developed, modified, and researched to provide a functional substitution that would aid the impaired user. These products enable people with functional difficulties to lead more productive and dignified lives, participating in education, the labour market, and social life. Our research aims to develop such a prosthetic hand to replicate the performance, functionality, appearance, and comfort of a natural hand. This product will be an accessible substitution with a user-friendly interface requiring little to no training and providing a high number of degrees of freedom. This means that the mechanical hand should be able to replicate most of the motion and functions that a natural hand can perform, like grasping various objects, tactile feeling, recognition, and manipulating different shaped objects. The links are also mentioned in the references section in the report. The prosthetic hand is an artificial device which is designed for the people with upper limb amputations to come up with some functions of the natural hands. The number of amputees in the developing countries is significantly greater than in developed countries due to minimum medical facilities and the popularity of illnesses that have been cured in the developed world. 

Uniqueness of the Technology:
Development of prosthetic hands have come a long way. They have moved away from solely meeting aesthetic purposes to having unique abilities resulting in the regained functionality that was once lost to trauma or amputation. Human movement is the driving force behind body-powered prosthesis. As the name suggests, precise body movements can trigger the hand’s actions, prompting basic open and close exercises via a cable system. 
ENRICH has a fast response timing approximately of 250 milliseconds. It can currently be one of the technologies which is cost-effective and could reach the larger part of the society. A body-powered prosthetic hand is a more traditional option and usually quick for the patient to learn to use. Unlike body-powered prosthetic hands, myoelectric prosthetic hands use your residual arm’s muscles and nerves to help train the prosthetic hand how to move. With this training, the prosthetic hand is able to learn patterns of behaviour from contracted muscles in the residual arm. A significant period of learning is required for a person to fully use this style of prosthetic. 

Competitive Technologies:
Lower prices are critical for improving access to bionic devices, but bionic hands don’t just compete on price. They also compete on technology. All bionic hands can grasp objects — that’s their primary purpose. What has differentiated one brand from the other for most of the past two decades are three core features: ease of use, dexterity, and durability. Until recently, more expensive hands generally offered superior control systems, which made them both easier to use and more dexterous. The commercial versions competition lies on the duration of response time. The different research prototypes from various universities around the world have developed the hand with different rates of response leading into upgradation and building a proper commercial product. It is also observed that most of the prosthetic hands use a greater number of EMG channels for controlling the hand. Correspondingly, computational load for decision making to understand the user’s interface for grasp opening and closing increases. So, it is preferable in the developed technologies, the channels are lower. Among the commercial version, BeBionic by Ottobock, Myo Select Hand by RSL Stepper are note-worthy.

Beneficiaries of the Technology:
The prosthetic hand is an artificial device which is designed for the people with upper limb amputations to come up with some functions of the natural hands. The number of amputees in the developing countries is significantly greater than in developed countries due to minimum medical facilities. Loss of upper limbs has many circumstances not only in the sense of physically but also in social and psychological department. By the year 2050, the number of people living with the loss of a limb would be close to 3.6 million. Among them, most of the upper limb amputees belong to weak socio-economic background. The World Health Organization estimates that, currently, 30 million people would benefit from an assistive prosthetic or orthotic device.  The use of extremities is essential for their communication and to perform day-to-day activities. Artificial hands and wrists are used to conduct everyday tasks such as washing, writing and picking various items to mitigate these effects and enable the amputee to return to normal life.

Details Regarding Testing of The Technology:
The first and main task to be solved by performing this research was to design a device in the form of a prosthetic arm which can be controlled by the amputees. The theme is to let the amputee perform simple daily tasks like holding and releasing objects. Since the prosthetic will be attached to the amputee’s forearm so the structure should be light and the size should be suitable for amputees. Another purpose of this project was development of a cost-effective prosthetic hand. A prototype prosthetic was created that has basic hand functionality, a durable yet lightweight structure utilizing 3D printing and a control unit, all available at a fair value for money. Here, in Tezpur University, it is in the prototyping stage and is tested in the demonstrative laboratory conditions. Besides these, the prototype in real subject application in taken into consideration. The testing is going on with amputees and the feedbacks are collected on a regular basis. However, the datalogging circuit prototype has been showcased but the testing and building of the circuit was not done yet. 

Potential for Technology Level Up-Gradation and/or Commercialization:
Hand prostheses should provide functional replacements of lost hands. Yet current prosthetic hands often are not intuitive to control and easy to use by amputees. Commercially available prostheses are usually controlled based on EMG signals triggered by the user to perform grasping tasks. Such EMG-based control requires long training and depends heavily on the robustness of the EMG signals. Rather than EMG based Prosthetic hands, the possible upgradation can be on hands with multi-modal sensors and camera or in the newest versions a distance sensor and IMU (Inertial Measurement Unit) on fingers which could correspond to different objects and accordingly create a grasp type on initiating with the EMG signals. The future goal is to develop prosthetic hands with semi-autonomous grasping abilities that lead to more intuitive control by the user. The developed prostheses would provide intelligent mechatronics including adaptive actuation, multi-modal sensing and on-board computing resources to enable autonomous and intuitive control. The hands are scalable in size and based on an underactuated mechanism which allows the adaptation of grasps to the shape of arbitrary objects. A resource-aware embedded system for in-hand processing of sensory data and control is included in the palm of each hand. To provide support for the user performing diverse activities of daily living (ADL), as for example food preparation, housekeeping or tool use amongst others, a prosthesis has to be reliable and versatile in terms of its grasping capabilities, i.e., it should be able to successfully perform a wide variety of ADLs. The user expects their prosthesis to be effortless and intuitive despite the inherent complexity of the mechatronics and control. The pivotal point of our hand development is therefore to endow prosthetic hands with intelligent grasping capabilities to support intuitiveness-of-use and to reduce the cognitive burden of the user. 
Talking about ENRICH, at this point of time, it is equipped with only one grasp type, i.e., power grasp. The further improvement includes incorporating precision grasp type into the prosthetic hand. Again, addition of the data logger circuit will help in real time data acquisition which will then be used to further improvement.
 
 
References-

[1] Kakoty, N.M., Kaiborta, M. and Hazarika, S.M., 2012. Electromyographic grasp recognition for a five fingered robotic hand. Int. J. Robot. Autom, 2, pp.1-10. 

[2] Joshi, D., Atreya, S., Arora, A.S. and Anand, S., 2009. Trends in EMG based prosthetic hand development: a review. Indian Journal of Biomechanics, pp.228-232. 

[3] Antfolk, C., Cipriani, C., Controzzi, M., Carrozza, M.C., Lundborg, G., Rosén, B. and Sebelius, F., 2010. Using EMG for real-time prediction of joint angles to control a prosthetic hand equipped with a sensory feedback system. Journal of Medical and Biological Engineering, 30(6), pp.399-406. 

[4] Juan Pablo S. Sola, Masudal, Haider Imtiaz, Ernetso Sola- Thomas, Designing a Prosthetic Hand as a College Freshman,2022 Conference paper ResearchGate

[5] Fajardo, J., Ferman, V., Cardona, D., Maldonado, G., Lemus, A. and Rohmer, E., 2020. Galileo hand: An anthropomorphic and affordable upper-limb prosthesis. IEEE access, 8, pp.81365-81377.

[6] Sánchez-Velasco, L.E., Arias-Montiel, M., Guzmán-Ramírez, E. and Lugo-González, E., 2020. A low-cost emg-controlled anthropomorphic robotic hand for power and precision grasp. Biocybernetics and Biomedical Engineering, 40(1), pp.221-237.

[7] Abarca, V.E., Flores, K.M. and Elías, D., 2019, April. The octa hand: An affordable multi-grasping 3d-printed robotic prosthesis for transradial amputees. In 2019 5th International Conference on Control, Automation and Robotics (ICCAR) (pp. 92-97). IEEE.

[8] Zhou, H., Mohammadi, A., Oetomo, D. and Alici, G., 2019. A novel monolithic soft robotic thumb for an anthropomorphic prosthetic hand. IEEE Robotics and Automation Letters, 4(2), pp.602-609.

[9] Atasoy, A., Toptaş, E., Kuchimov, S., Gulfize, S., Turpcu, M., Kaplanoglu, E., Güçlü, B. and Özkan, M., 2018, August. Biomechanical design of an anthropomorphic prosthetic hand. In 2018 7th IEEE International Conference on Biomedical Robotics and Biomechatronics (Biorob) (pp. 732-736). IEEE.

[10] TowerPro (2014). MG958 - TowerPro. [online] Available at:    www.towerpro.com.tw/product/mg958/ [Accessed 26 Jul. 2022].

[11] ESP32 (2022). ESP32 Series Datasheet. [online] Available at: www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf [Accessed 27 July 2022].

[12] ESP8266EX (2022). ESP8266EX Datasheet. [online] Available at: https://espressif.com/sites/default/files/documentation/0a-esp8266ex_datasheet_en.pdf [Accessed 27 July 2022].




