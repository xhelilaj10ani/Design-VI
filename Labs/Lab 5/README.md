# CPE 322 - Lab 3
## Paho - MQTT
### Dritan Xhelilaj </br>
"I pledge my honor that I have abided by the Stevens Honor System."

---
## Installation
On Windows, I started by downloading and installing Mosquitto from the official website. After the installation, I updated the system's environment variables by going to ***System Properties > Environment Variables***, then editing the ***Path*** variable to include ***C:\Program Files\Mosquitto***. This ensures that the Mosquitto executable can be accessed from the command line. </br>

---
## Setting Up Terminals and the Running Scripts
I launched two terminal windows and ran a series of commands in each: </br>
- `cd ~/iot`
- `git pull`
- `cd lesson5` </br>
![5l1](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%205/5l1.png) </br>

Navigating to the ***iot*** directory and pulling from Git ensured my local copy of the repository was up to date. After that, I moved into the ***lesson5*** folder where the necessary Python scripts were stored. Once everything was set up, I executed `python pubcpu.py` in one of the terminals. </br>
![5l2](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%205/5l2.png) </br>

In the second terminal, I similarly ran `python subcpu.py` after completing the setup.
![5l3](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%205/5l3.png) </br>

Executing these commands resulted in the terminal running `pubcpu.py` publishing data about my CPU. Meanwhile, the terminal running `subcpu.py` acted as a subscriber, receiving and displaying the data sent by `pubcpu.py`. The image below illustrates this interaction, with the publishing terminal shown on the left and the subscribing terminal on the right.
![5l4](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%205/5l4.png) </br>

---
## Summary
This lab taught me how to utilize Paho-MQTT to send messages from one terminal and set up another terminal to subscribe and receive those messages.
