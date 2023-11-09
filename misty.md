### Misty Starter Guide

***


## Connecting to the Misty

First things first, you’ll want to turn the misty on!![](https://lh6.googleusercontent.com/mbRNtHa4L6vDi5cdYUGeltBawvv_94_ZXBiHIxlSnY2JeHn87eFOgaVXJH3qNLB_6Ia3WlJTuAoU7ptEK9MBrPv9j7WJO8aGpnYS26MA_kJdq3NTJ8mlAW6kvYzxc0LxBrRu7VQVkEmKQ2kkO6-Qpg)

\
![](https://lh5.googleusercontent.com/gBmpK3zuBOlOS4wzjaMfF6cFYF2vkUQy81slsMvd5CjdRi9VritopSQ_WoXt63YEKrtvwTMZNDtvz1ifThAb2_HUBPbMMVOlHstUTpiU1IaC36njScbtXJ1QjDFbWBpGk_TeHIom1rzTquDtwCh8tQ)

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

4. Open that file. Set the first line to ‘tufts\_eecs’ and the second line to ‘foundedin1883’. It should look like this![](https://lh6.googleusercontent.com/wiPx8Rt8g4WH4Ep1VW6EDgH2yaipHEA2dR9mVCDL4mvAZxCHCfLiS-J-yvO7FegwqgmocDyj8KRMoc5DO9-LX1sZJHFXlRQseFnPYYMtEW9j2JSg3Wpvv54wqmCDepY29saefxE2L_ndHKSokJhZhw)

5. Save the file with this information within it. Eject the USB. ![](https://lh6.googleusercontent.com/1v-JDE6i9eR68fqVYrABXV29CqzkKJvKVpvWXAXropM3s5LLTbQZy650ZK6G_0HLES09fXbxgL9zX_sWfJKHK_11mItTYaljh29gRidftc9-iNerPaW1r4AKs8I_w_gTo-ta72T2zcGevLslnQRBhA)

6. Plug the USB into the Misty! The USB port is a little hidden on Misty’s back.

7. Give the Misty some time to process that information–the documentation says at least 60 seconds.

8. Then, remove the usb drive from the Misty. Plug it back into your computer. It should now have a file within the ‘misty’ folder that says ‘onboard.txt’, this file will have the Misty’s ip address. 

Now that you have the Misty’s ip address you can use various methods to program the Misty! You can see the various methods of programming the misty at: <https://docs.mistyrobotics.com/misty-ii/robot/misty-ii/>

#### Misty with Python

It's up to you how you want to program the Misty. There are multiple methods you can find here: <https://docs.mistyrobotics.com/misty-ii/robot/misty-ii/>. There seems to be an issue with getting the Misty to speak. If you do want to get the Misty to speak, there's a workaround on our github <https://github.com/Tufts-Robot-Teaching-Lab/MistyPySpeechWorkaround>.
