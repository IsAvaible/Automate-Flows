# SMS Control
Implements different commands to control your phone via SMS messages send to the phone running this flow.

Use the "# Test" flow beginning if you want to test a command.

——————

Abbreviations:
b=back facing cam 
f=front facing cam (default)
l=flash (default: no flash)
n=phone number

‹...› Should be replaced with the value.

Commands:
- !ringOnp:‹pwd›
Turns on ringer mode

- !ringOffp:‹pwd›
Turns off ringer mode

- !playSound‹time (sec)›p:‹pwd›
Plays a sound at full volume.

- !recordVideo‹time (sec)›‹b/f›‹l›p:‹pwd›
Records a video for specifed time using specified camera and uploads it to GDrive.

- !recordAudio‹time (sec)›
›p:‹pwd›
Records an audio for specifed time and uploads it to GDrive.

- !takePicture‹b/f›‹l›p:‹pwd›
Takes a picture with specified camera and uploads it to GDrive.

- !locationp:‹pwd›
Replies with the current location data.

- !notification‹n:number›p:‹pwd› ‹message›
Posts a persistent notification. If n is specifed allows calling the number from the lockscreen.

- !lockp:‹pwd›
Locks the phone.

- !guardp:‹pwd›
Guards the phone: Monitors failed login attempts and sends a image taken with the front facing camera and the location on fail. Prevents disabling airplane mode. 

- !wifip:‹pwd›
Turns on Wifi.

- !testp:‹pwd›
Replies with a message.

- !helpp: ‹pwd›
Replies with this documentation.

——————

You may need to adjust the XPath of the Input Touch block (198) that disables the airplane mode if your system language is not english.
Use this flow to create a new XPath: https://llamalab.com/automate/community/flows/40593

Most commands can also be triggered by different keywords. Because of space reasons these are not printed here, but you can find them inside the flowchart (fX #findAll...).

——————

Examples:
• !recordVideop:0000
» Records a 10sec video with the front facing cam.

• !takePictureblp:0000
» Takes a pic with the backfacing cam and flash enabled.

• !notificationn:+492739193718p:0000 Please call by pressing the button below.
» Posts a notification on the lockscreen. 


# Flowchart
![Image of the Flowchart](SMS_control.png)