# CPE 322 - Lab 9
## YANG
### Dritan Xhelilaj </br>
"I pledge my honor that I have abided by the Stevens Honor System."

---
## Installment of pyang and PlantUML
To install pyang and PlantUML I used the following commands: </br>
- `pip3 install -U lxml pyang`
- `pip3 install -U plantuml`

![inst](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/inst.png) </br>

---
## Pyang
I created a lab9 folder using `mkdir lab9` command. then I used the commands below to copy intrusiondetection.yang into lab9 and switch to the lab9 directory: </br>
- `cp ~/iot/lesson9/intrusiondetection.yang ~/lab9`
- `cd ~/lab9`

The following commands were then run to generate both intrusiondetection.yin and intrusiondetection.uml, while also displaying the contents of the intrusiondetection file in its .yang, .yin, and .uml formats.
- `cat intrusiondetection.yang`
- `pyang -f yin -o intrusiondetection.yin intrusiondetection.yang`
- `cat intrusiondetection.yin`
- `pyang -f uml -o intrusiondetection.uml intrusiondetection.yang --uml-no=stereotypes,annotation,typedef`
- `cat intrusiondetection.uml`

Shown below are the contents of the intrusiondetection file in all three formats: </br>

### .yang: </br>
![ya1](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/ya1.png) </br>
![ya2](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/ya2.png) </br>

### .yin: </br>
![yi1](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/yi1.png) </br>
![yi2](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/yi2.png) </br>

### .uml: </br>
![uml](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/uml.png) </br>

---
## PlantUML
I used the command `python -m plantuml intrusiondetection.uml` to generate a sequence diagram in PNG format. After that, I manually downloaded and installed Pinta and GIMP using their .exe installers from their official websites. Then the following command was used to display the .png image:
- `Start-Process .\intrusiondetection.png`

### .png image:
![png](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%209/png.png) </br>

---
## Summary
In this lab, I examined the appearance of a file in .yang, .yin, .uml, and .png formats. The pyang tool proved useful for converting YANG models into YIN or UML formats, while PlantUML was effective for generating PNG diagrams from UML files.
