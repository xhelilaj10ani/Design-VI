# CPE 322 - Lab 6
## Node.js and Pystache
### Dritan Xhelilaj </br>
"I pledge my honor that I have abided by the Stevens Honor System."

---
## Node.js
Since Node.js was already installed on my Mac, I was able to jump straight into running the scripts. I did this by executing the following set of commands: </br>
- `cd ~/iot/lesson6`
- `node hello-world.js`
- `node hello.js`
- `node http.js`
![6l1](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%206/6l1.png) </br>

Each web page demonstrated different server behaviors. As shown in the image above, ***hello-world.js*** produced no visible server output. In contrast, ***hello.js*** logged messages like "response end call done" and "request end event fired" in the terminal whenever the page was refreshed. Finally, ***http.js*** kept track of and displayed the number of times the page had been refreshed.

The images below illustrate the appearance of each web page:

### hello-world.js
![6l2](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%206/6l2.png) </br>

### hello.js:
![6l3](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%206/6l3.png) </br>

### http.js:
![6l4](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%206/6l4.png) </br>

---
## Pystache
I installed Pystache on my Mac by running `pip3 install pystache`. After that, I navigated to the appropriate directory and ran a series of commands to execute `say_hello.py`, which utilizes the `say_hello.mustache` template:
- `cd ~/iot/lesson6`
- `cat say_hello.mustache`
- `cat say_hello.py`
- `python3 say_hello.py` </br>

The output from these commands is displayed below:
![6l5](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%206/6l5.png) </br>

---
## Summary
Through this lab, I gained experience in running web pages with Node.js and learned how to work with Pystache, the Python version of the Mustache templating engine.
