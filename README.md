# Drayton Wiser Hub API Async v0.1.2

This repository contains a simple API which queries the Drayton Wiser Heating sysystem used in the UK.

The API functionality provides the following functionality to control the wiser heating system for 1,2 and 3 channel heat hubs
The API also supports Smart Plugs and initial basic functionality for Shutter and Lights

## Installation

## 1. Find your HeatHub Secret key

Reference [https://it.knightnet.org.uk/kb/nr-qa/drayton-wiser-heating-control/#controlling-the-system](https://it.knightnet.org.uk/kb/nr-qa/drayton-wiser-heating-control/#controlling-the-system)

1. Press the setup button on your HeatHub, the light will start flashing
Look for the Wi-Fi network (SSID) called **‘WiserHeatXXXXXX’** where XXXXXX is last 6 digits of the MAC address
2. Connect to the network from a Windows/Linux/Mac/Android/iPhone machine
3. Execute the secret url :-)
   * Open a browser to url `http://192.168.8.1/secret`

   This will return a string which is your system secret, store this somewhere. If you are running the test script simply put this value , with the ip address of the hub, in your wiserkeys.params

4. Press the setup button on the HeatHub again and it will go back to normal operations
5. Copy the secret and save it somewhere.

## 3. Find Your HEATHUB IP

Using your router, or something else, identify the IP address of your HeatHub, it usually identifies itself as the same ID as the ``WiserHeatXXXXXX``

Alternatively see the test_api_discovery.py file for how to use the api to discover your hub

## 4. Add values in you params.py to run tests

Create a file called params.py and place two lines, one with the wiser IP or hostname and the other with the secret key.
e.g.

```code
HOST=192.168.0.22
KEY=ABCDCDCDCCCDCDC
```

## 5. Run the sample

To help understand the api simply look at the test sample code ```tests/test_api_properties.py```, ```tests/test_api_methods.py``` or ```tests/test_api_discovery.py``` and the fully commented code.

## 6. Documentation

Documentation available in [info.md](https://github.com/msp1974/wiserHeatAPIv2/blob/master/docs/info.md) in the docs directory and within comments in the code

## Changelog

### 0.1.0

* Initial asyncio release
