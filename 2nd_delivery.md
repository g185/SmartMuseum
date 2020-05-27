# 2nd Delivery

## Comments received and decisions

-*Is face recognition too much for proximity?*
Even if face recognition was a challenging part of our project, we decided that it was really an utopy to run it on a constrained device without really long latency time. We decided to use proximity sensors that were better under a lot of perspectives.

-*Customization for kids vs adults could be a nice feature.*
Sure, it will be an important part of our project. The function that detects heights of the user is born to give a different audioguide to the kids. "Message in the bottle" functionalities will be an important feature for kids interactivity.

-*Include the designer in the README.*
We did it.


## Changes made to design, architecture and evaluation plan since 1st delivery
Design: The design was impacted by the decision to change sensors. We now will use proximity sensors in order to detect the presence of people. In order to have a different audioguide for kids we will detect height of the user. The motivations for this choiche are different: The difficulty of face recognition would lead the processing to last too much time. 

The price of the sensors, processing power, energy consumption and performances will all benefit from this change.

We also introduced the functionality "Message in the bottle" so that the users will be able to leave a short audiomessage to the next visitors. 

Architecture:
The main difference from the architecture we thought at the beginning, is in the decision to leave AWS for Thingsboard. We evaluated the costs of the project, and thingsboard offered the functionalities we needed to a lower price. The main functionality in fact is a clean looking dashboard with a private access.
For what regards the boards-sensors architecture, we eliminated the use of the camera, introducing 2 height sensors in order to detect proximity and height of a visitor. We will also use the speaker via the AUDIO-OUT AUX port of the board. We will then introduce the buttons for the Message functionalit.

Evaluation: 
Some evaluation of the new sensors include the sensor detection distance and latency, but overall the final product evaluation remains the same.

The evaluation process of the cloud service remains the same with Thingsboard: we will test the latency of the mqtt messages.

## Brief presentation of the technical work done since 1st delivery
We started with a really long period of testing of different solutions and applications in order to make the idea of Face Recognition possible. We experienced different problems, specially with the installation of OpenCV library. We spend different days in the search of a solution: We started developing OpenCV on MBED-OS but [OpenCV library](https://os.mbed.com/users/joeverbout/code/main/) seems corrupted. We have then found an interesting project called [EMBOX](https://github.com/embox/embox) where we ended up spending 2 days directly talking to the founders, that at the end said that object detection was causing problems with their OS and are now working to fix the source code. We searched and tried also different (but very few) solutions present online, and we finally concluded that this process was not leading us to a feasible solution.

After that, we started developing the new Proximity Sensor idea for the project. We started using the proximity sensor library for MBED OS and succeded to develop a little demo, that is able to detect if a person is standing in front of the sensor. For this reason we developed an algorithm that is able to correctly detect a person if standing at 1.5m from the statue. More on the Algorith is shown on the presentation of the technical work.

We than have introduced the MQTT functionalities. We used the MQTT library of MBED OS and started to dig into the settings that made possible a correct connection. Once it was possible we started to design an algorithm that sent a message with the presence of a person in front of the proximity sensor. A demo will be shown in the presentation video of the tecnichal approach done so far. 

Finally, we tested the functionalityes of the buttons, in order to trigger different signals to the board: They will be later useful to start and reproduce the "Message in the bottle".

## List of functionalities that are missing and will be completed for the final delivery

-dashboard ciotta

-Manager che se connette e mette la roba sua

-miglioramenti a tutto

-now the board distinguish from kid to adult  and plays different tracks da finire


## Evaluation conducted since the 1st delivery

-evaluated sensors accuracy and other and board


## Expected evaluation for the final delivery

-quelle che mancane