
```
        ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄   ▄▄▄▄▄▄▄▄▄▄▄  ▄▄        ▄  ▄▄▄▄▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄▄▄ 
       ▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌▐░░░░░░░░░░▌ ▐░░░░░░░░░░░▌▐░░▌      ▐░▌▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌
       ▐░█▀▀▀▀▀▀▀█░▌ ▀▀▀▀█░█▀▀▀▀ ▐░█▀▀▀▀▀▀▀█░▌▐░█▀▀▀▀▀▀▀▀▀ ▐░▌░▌     ▐░▌▐░█▀▀▀▀▀▀▀▀▀ ▐░█▀▀▀▀▀▀▀▀▀ 
       ▐░▌       ▐░▌     ▐░▌     ▐░▌       ▐░▌▐░▌          ▐░▌▐░▌    ▐░▌▐░▌          ▐░▌          
       ▐░█▄▄▄▄▄▄▄█░▌     ▐░▌     ▐░▌       ▐░▌▐░█▄▄▄▄▄▄▄▄▄ ▐░▌ ▐░▌   ▐░▌▐░█▄▄▄▄▄▄▄▄▄ ▐░█▄▄▄▄▄▄▄▄▄ 
       ▐░░░░░░░░░░░▌     ▐░▌     ▐░▌       ▐░▌▐░░░░░░░░░░░▌▐░▌  ▐░▌  ▐░▌▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌
       ▐░█▀▀▀▀▀▀▀▀▀      ▐░▌     ▐░▌       ▐░▌▐░█▀▀▀▀▀▀▀▀▀ ▐░▌   ▐░▌ ▐░▌ ▀▀▀▀▀▀▀▀▀█░▌▐░█▀▀▀▀▀▀▀▀▀ 
       ▐░▌               ▐░▌     ▐░▌       ▐░▌▐░▌          ▐░▌    ▐░▌▐░▌          ▐░▌▐░▌          
       ▐░▌           ▄▄▄▄█░█▄▄▄▄ ▐░█▄▄▄▄▄▄▄█░▌▐░█▄▄▄▄▄▄▄▄▄ ▐░▌     ▐░▐░▌ ▄▄▄▄▄▄▄▄▄█░▌▐░█▄▄▄▄▄▄▄▄▄ 
       ▐░▌          ▐░░░░░░░░░░░▌▐░░░░░░░░░░▌ ▐░░░░░░░░░░░▌▐░▌      ▐░░▌▐░░░░░░░░░░░▌▐░░░░░░░░░░░▌
        ▀            ▀▀▀▀▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀▀▀▀   ▀▀▀▀▀▀▀▀▀▀▀  ▀        ▀▀  ▀▀▀▀▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀▀▀▀▀ 

                             Monitor illegal wireless network activities.
              ------------------------------------------------------------------------------

```

<p align="center">
<img src="https://img.shields.io/badge/Python-2-yellow.svg"></a> <img src="https://img.shields.io/badge/license-GPLv3-red.svg">
<a href="http://www.blackhat.com/eu-17/arsenal/schedule/#wipi-hunter---wifi-pineapple-activities-detection-9091"><img src="https://rawgit.com/toolswatch/badges/master/arsenal/2017.svg"></a>
</p>

#### Purpose

Monitor  **illegal wireless network activities.**

+ Similar SSID broadcasts
+ Same SSID broadcasts
+ Calculates unencrypted wireless networks density
+ Watches SSID broadcasts at the blacklist.

#### Capabilities (Now)

+ Calculates Unencrypted wireless network density
+ Finds same ssid, different encryption

#### Working Principle for PiDense

+ Collects all the packets from Wireless Networks.
+ Analyzes all the beacon packets. 
+ If PiDens detects more than defined threshold of OPN number, or different encryption with same SSID info ;
+ Logs the activity with some extra information within defined template.

#### Soon to be added features 

+ Blacklist SSID analysis
+ Company name setting for illegal wireless attack activities (Monitoring)

#### Example
+ Video: https://www.youtube.com/watch?v=hsMz6zM-yks


### --------------------------------------------------------------------------------

### Usage

#### Requirements

* **Hardware:** TP LINK TL-WN722N
* **Modules:** scapy, time, termcolor, argparse

#### Kali Linux:

Download PiDense:

`git clone https://github.com/WiPi-Hunter/PiDense.git`

Install Python librarie(s):

`pip install termcolor`

It's done!

Run the program with following command: 

Monitor mode:

```python
airmon-ng start interface(wlan0,wlan1) (Monitor mode)

or 

ifconfig wlan0 down
iwconfig wlan0 mode Monitor
ifconfig wlan0 up
```

Run:

```python
cd PiDense
python pidense.py -h
```
