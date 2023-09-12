### Misty Starter Guide

***


## Connecting to the Misty

First things first, you’ll want to turn the misty on!![](https://lh6.googleusercontent.com/FsDBxN97uThnqzZy0JJZaU2a6Ybfn07yeMV3KAr7Wn2nwvbKvcYWl5py9lPyigvrAbvFSnv_2J5lV21_BC41IHRqXiqBt1dk9mNlGoIX_ErU2zhnCn4_DTzhEv1oxRcdY_PR30W-KqlqABBSOi3sLw)

\
![](https://lh4.googleusercontent.com/4AVjuFrnd39GmkGI_7-JnJaiRBo9akDd0XNP6gD-OSb6qSYAsTxw3Y1FqjBXW_Lwd85AkUeXrII-S2na7yDd43lo3oLs9nvnfKG-OtIXb4vJhEMZXdkHV9WGZB2Y9bfUS9X0rSCxh0Vj7xbneDzYew)

The power switch is at the bottom of the robot to the back.

You can tell the robot is on because you will see lights turn on (and most likely hear a whirring noise). If nothing happens when turning it on, try charging it. 

You can see the full usage guide of a misty robot, here: <https://docs.mistyrobotics.com/misty-ii/robot/misty-ii/>

In order to connect to Misty with a mobile app, you will need to have an android device. Using the Misty app can give you information about the Misty as well as it’s IP, but it’s not the only way you can find out should you not have an android!


#### Connecting to a Misty without the Android App

I personally struggled using the app (I have an android, but it kept crashing!) HOWEVER, the app is incredibly useful in that it gives you the Misty’s IP Address– something vital no matter your method of programming the misty.

Connecting to the Misty without an Android App requires the use of a USB (aka USB Drive). 

1. First you’ll want to format the usb drive as “FAT”.

   1. I used this guide to do so on linux: <https://www.tutorialspoint.com/how-to-format-usb-drives-in-linux>

   2. On linux, I essentially plugged the USB in, right clicked it, and then pressed “Format”, making sure to check the “FAT” option.

   3. To do this on other operating systems see these guides:

      1. Mac: <https://support.nadelectronics.com/hc/en-us/articles/360000158588-How-to-Format-a-USB-flash-drive-on-a-Mac-to-MS-DOS-FAT->
      2. Windows: <https://www.howtogeek.com/902632/format-usb-flash-drive-to-fat32-windows/>

2. After formatting your usb drive, in the root of that drive (aka the base folder of the flash drive), create a folder/directory called ‘misty’ (NOTE: do not add the quotes)

3. Inside the ‘misty’ folder/directory create a .txt file called ‘wifi.txt’.

4. Open that file. Set the first line to ‘tufts\_eecs’ and the second line to ‘foundedin1883’. It should look like this![](https://lh3.googleusercontent.com/kzXJzaF4ZYlC7xCLx4Ng4cGFAOissIJUi1ZAcSQwbk8UXhicxIZO1OYHllTceYRliAngwWuWzyF1Aa4jWiuh5RDPdfIYFSQZIUTSed16X2rJFEiuZ_eJPHjWnjmybVmWUmSz4ffdta7vdsDS4b1-Zg)

5. Save the file with this information within it. Eject the USB. ![](https://lh6.googleusercontent.com/15Vmzgh7oCn6j-wx-7lde4XcgjTuYOWwtpbW0nw1yNYvxILEIKwTYJgb52DG3mwBMH39kiRcYQuEyd60MKfU-17vNVBNR2Y8eW2ras1UUG7gg34LRoGRUCItwS6ZYzFNecZMRwAb19mg2pMUXmU3KQ)

6. Plug the USB into the Misty! The USB port is a little hidden on Misty’s back.

7. Give the Misty some time to process that information–the documentation says at least 60 seconds.

8. Then, remove the usb drive from the Misty. Plug it back into your computer. It should now have a file within the ‘misty’ folder that says ‘onboard.txt’, this file will have the Misty’s ip address. 

Now that you have the Misty’s ip address you can use various methods to program the Misty!
