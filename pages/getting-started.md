---
layout: page
comments: true
show_meta: false
title: "Getting Started"
subheadline: "A Step-by-Step Guide"
teaser: "This is a step-by-step guide to preparing your computer for the IoT Labs."
header:
   image_fullwidth: "header_homepage_13.jpg"
permalink: "/getting-started/"
---
# Preparing for the IoT Labs
The labs in this series build on each other to enable you to prototype your own Internet of Things (IoT) devices. 
In this lab you will use Node.js and an open source framework for interacting with hardware called Johnny-Five, 
which works as a baseline control kit for Arduino-based projects. This enables you to write applications in JavaScript 
that can run either on your computer connected to an Arduino board or directly on the board itself (if the board has 
a Linux distribution, like the Arduino Y&uacute;n and Linino ONE).

We chose the Arduino Y&uacute;n for this workshop because it has both a Linux distribution and on-board Wi-Fi, although several 
of the labs can be completed using any Arduino board because the Node.js code will run on your laptop and use the Arduino 
over USB. If you want to deploy the applications you build to the Arduino, you will need a board that has a Linux distro
(such as the Y&uacute;n or the Linino ONE).

## Bill of Materials
To prepare your development environment for this lab series you don't need anything other than a computer. Each lab in the
series will have a bill of materials indicating what is required for that lab.

If you want to prepare yourself further before the labs you can acquire the following:

0. [Arduino Y&uacute;n](http://www.arduino.cc/en/Main/ArduinoBoardYun) 
1. USB to micro-USB cable 
2. An Arduino compatible starter kit w/o the board (1)
	1.	An example would be the [SparkFun Inventor's Kit (for Arduino Uno) - V3.2](http://www.sparkfun.com/products/13154) (it comes with an Arduino Uno R3, which you can use only in some of the early lessons)

## Install the Arduino IDE
While you won't use the Arduino IDE very much in the set of labs, it is necessary for a couple of things. For one thing, installing the Arduino IDE also installs the USB drivers for the Arduino board.

Go to http://www.arduino.cc and follow the links to download the latest version of the Arduino IDE. Make sure that the checkbox for the USB driver is selected during install (it typically is by default).

## Install a Code Editor
If you don't already have one installed, pick a text/code editor. Feel free to use anything you like, provided it won't inject any extra text into your files.

Some Options:

* [Visual Studio Code](http://code.visualstudio.com/) (this is our preferred tool)
* [Visual Studio](http://www.visualstudio.com/) 
* [Sublime Text](http://www.sublimetext.com/) 
* [Eclipse](http://www.eclipse.org/downloads/) 
* [Notepad++](http://notepad-plus-plus.org/)

## Install Git
Some of the tools you will be using in this workshop require Git. The download link can be found [here](http://git-scm.com/).

### Windows Only
During the Git install, check the option to _Use Git from the Windows command prompt_.

If you don't choose this option, after you have installed Git, you need to add the path to get to your development environment. To do that, add the path to Git to the PATH environment variable.

1. Open _Control Panel_ > _System and Security_ > _System_ then click on _Advanced Settings_.

2. Click on the _Environment Variables_ button toward the bottom of the dialog.

3. Locate the User variable named __PATH__ and double-click it.

4. Append the following to the Variable value textbox (if you installed Git to a different location you will need to modify this value accordingly):
	<pre>
		;C:\Program Files (x86)\Git\bin;C:\Program Files (x86)\Git\cmd
	</pre>

5. Click _OK_ to close the Edit User Variable dialog.

6. Click _OK_ to close the System Properties dialog.

7. Close any remaining dialogs/windows (i.e. Control Panel).

## Install Node.js
In the labs you will write small programs that will run on your computer, connected to your Arduino (these can also be deployed to run solely on your Arduino Y&uacute;n). These programs will be written in JavaScript and will be built on Node.js. If you are not familiar or experienced with Node.js, don't worry. You will learn everything you need to know for these labs in these labs. 

Follow the [instructions here to install Node.js](http://nodejs.org/) on your computer.

## Install Bower
Bower is a package manager similar to the Node Package Manager (NPM). For these labs we will use both NPM and Bower. You install Bower using NPM. 

On Windows, open the Node.js command prompt and type the following:
<pre>
	npm install -g bower
</pre>

On Mac OS X open Terminal and type the following:
<pre>
	sudo npm install -g bower
</pre>

## Install Apache Cordova and Cordova Icon

### Apache Cordova
Apache Cordova is an open-source mobile development framework. It allows you to use standard web technologies such as HTML5, CSS3, and JavaScript for cross-platform development, avoiding each mobile platforms' native development language. Applications execute within wrappers targeted to each platform, and rely on standards-compliant API bindings to access each device's sensors, data, and network status.

On Windows, open the Node.js command prompt and type the following:
<pre>
	npm install -g cordova
</pre>

On Mac OS X open Terminal and type the following:
<pre>
	sudo npm install -g cordova
</pre>

### Cordova Icon

Cordova Icon is a tool that provides automatic icon resizing for Cordova apps.

On Windows, open the Node.js command prompt and type the following:
<pre>
	npm install -g cordova-icon
</pre>

On Mac OS X open Terminal and type the following:
<pre>
	sudo npm install -g cordova-icon
</pre>

## Install Johnny-Five
Johnny-Five is an open source JavaScript framework that provides a simple object model for interacting with an Arduino-based board and the sensors and devices you connect to it. 

Once you have Node.js installed, install [Johnny-Five](http://www.npmjs.com/package/johnny-five) using NPM.
On Windows, open the Node.js command prompt and type the following:
<pre>
	npm install johnny-five
</pre>

On Mac OS X open Terminal and type the following:
<pre>
	sudo npm install johnny-five
</pre>

## Install Nitrogen
Nitrogen is a messaging service that will act as a gateway for your Thing connecting to Azure. Nitrogen supports connecting devices via Message Queue Telemetry Transport (MQTT) or using the Nitrogen Node.js client library (you can learn more about MQTT here). You install Nitrogen using NPM.

On Windows, open the Node.js command prompt and type the following:
<pre>
	npm install -g nitrogen-cli
</pre>

On Mac OS X open Terminal and type the following:
<pre>
	sudo npm install -g nitrogen-cli
</pre>

## Set Up a Development Directory
The last thing to do is prepare a place to save all of your work in the labs. I recommend an easy to navigate to directory with a relatively short path. Create a new folder/directory for the workshop - I recommend:

Windows
<pre>
	C:\Development\IoTLabs
</pre>

Mac OS X
<pre>
	~\Devleopment\IoTLabs
</pre>

That's it for now. You are ready to start the [first set of labs](/iotlabs/lab001/).
