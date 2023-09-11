# Tufts-Robot-Teaching-Lab.github.io

### TurtleBot Docs

### Turtlebot Starter Guide

***


#### Connecting to the Turtlebot

1. Make sure that you’re logged onto the ‘tufts\_eecs’ wifi network

   1. The password is ‘foundedin1883’

<!---->

2. Turn on the turtlebot (on/off switch is on the right of the base)

![](https://lh6.googleusercontent.com/JEc3fQwaRsewgsZ68ouxqawiVNU8puICoDrSsUst99SrjbeHIM3VLsH2dPUX1ky5gSrMYY0s5JM75vb1VkQXmtl2n9NTJscSSswK7hd5PKFvwiiVSHt8g3kxgWhSS8glOCl3wCPZ5Kj88cS8awMT)

3. On the turtlebot, type ‘ifconfig’ and make note of the ip address. It should look something like this:

 ![](https://lh4.googleusercontent.com/1j0WVSit0brY_DRy8sLuPuSdSwQK174gkrqtdQCR0NTDtgUr5_X1hV2vBZ5iyzuSMxVZsonTemKo-NBvTKoMxoLafdTrrTvrK0oYWaOmA1NGuGGm6CWXDDBpgu4L97dlLDvCuQIyOpBR8w2ed0Rs)

\
\


4. In the terminal on your computer, type ‘ssh turtlebot@\<ip\_address>’. It should look like this: ![](https://lh6.googleusercontent.com/aTOYAj2O8wkjBwCiHTps-AQ3lg91JBwYvfM-7Fx0_OnCKIObbKMM98z7EQiJQempcQWvCmHH5sQ8XY4l1oiLq9TvwWi6BeOlOoHpNW6ZQc5yDnuUUazegOQvHnDXtWKWOHnOVGIHStqbQsqrKHAy)

You will have to enter the password for the turtlebot, which is ‘turtlebot’.


#### Running Files on the Turtlebot

5. In the terminal you’ve ssh’d into on your computer, in a new tab type ‘roslaunch turtlebot\_bringup minimal.launch --screen’![](https://lh4.googleusercontent.com/5j_0aNDo4qeqY9RhptNpAe0bfzirPe7rVQ57WQA3nLFhi5805KRJVBTP-_gZTCMj-b_i_3gNpqbk56WPbP2lDPVplSSO9M6mvfJbZY2zF0jlppogdQdQz5xgJ8MMAY37udPIr2GuSUCp04ksSRGt4Q)

<!---->

6. To teleoperate the turtlebot with the keyboard, ssh into a new tab on your computer, then run ‘roslaunch turtlebot\_teleop keyboard\_teleop.launch’

![](https://lh6.googleusercontent.com/A9uOzfzetY5R-6vXLy9LLRkOHDs9Rl_Ux6tlHhQf6HqJ-IBAIOJpIggp2oAdBgUvuRiu0GizS5_BfliczG3awoS5H7GjQvf4dO3mXuuTq1l0XmNoa9YviOx7ov0vcl7AoStE8kRIrIE9zJ76jF5n)

Use the keys below to control the turtlebot:

![](https://lh3.googleusercontent.com/boF20vUDfr4_IAw4fQKqtyKBOWAd7TxcDGKI1Dk8Mz2QGvh5QqdUH5TX5sriEy0IDQnrVhzidn7f3LBaoUu-k_SdpAIj-kpXKB7U73lcwMGxvCJUS3Yq4zwcWpvk5bJ-xjLwhlUv-Z8l0eX2cstN)

7. To copy files from your computer to the turtlebot, on your computer (**NOT** in the terminal you’ve ssh’d into) type ‘scp -r \<source> \<target>’

   1. An example of this is: ‘scp -r example\_folder/example\_file.py turtlebot@\<ip\_address>’.
   2. To specify further in your target you can add a colon (‘:’). An example of this is ‘scp -r example\_folder/example\_file.py turtlebot@\<ip\_address>:specific\_folder/’
   3. Something to note: You don’t need to ssh into the turtlebot to run scp, but it’s usually useful if you have a terminal connected to the turtlebot so you can check if the files have correctly copied over.


#### Launching the Camera

8. On your computer, type \`roslaunch astra\_camera astra.launch\`

✧･ﾟ: \*✧･ﾟ:\* Troubleshooting  Permissions✧･ﾟ: \*✧･ﾟ:\*

Suppose that you try to run the line above to launch the camera, and you get a message that looks something like this:

![](https://lh4.googleusercontent.com/XkL4Nu--Tv5vxJK_w0S47sEIHLgdk7rccV1Y5K2RYs_MMgAb5avD-0PQEbw1VP5Azc6Rb_Cuo5ILXKbOanqgCiZhKKpPYmQk0zLvAvH8SSMU9r-6VTO8EOw8mTfO4HtWZq_fXjWZkNFUcwmw_m-4Yg)

Try running the command \`rostopic hz /camera/color/image\_raw\`. Ideally, the output should look like this: 

![](https://lh3.googleusercontent.com/_4Yhceb2ONPbrA0qZlHSqd7wt-QhAIn0Qd3MVdGAeuJb1xp-4KQtT1wkhSb-1vvI_Yg54Rro-nTpxbQK3zI9MFci_gvbxubyldBJ6np-ynCEZb90xQiMp-dIqbkLGHl6oOx6XtA4VF-5PT-lGp3pSQ)

If the output **doesn’t** show any data, then you may need to adjust your permissions: 

1. On your computer, in a terminal that has **not** been ssh’d into, open the file _/etc/hosts_ by running \`code /etc/hosts\`. On a new line, type \`\<turtlebot\_ip\_address> \<turtlebot\_hostname>\`. Save the changes. The file should look like this:

 ![](https://lh5.googleusercontent.com/3o_prvttJeAcnXHU2LUvseOzYBZyu9gVXqCuzPpsFKCIizrFFdSNybj6aUNfIucgrjmGs7696HqQ0_yIl0wZsDEUeu3SpPdugibul09oAgDMG077Oz82YncD8CY-CKghZve61-_mq4l5NB1nnuaUWQ)

2. Next, find the ip address of your own computer by running ‘ifconfig’ in a terminal that has not been ssh’d into.![](https://lh6.googleusercontent.com/OVccKd69SgGY48uNTOJsO9Ni_sZMjN7uYTFE1PxHSbDJ9PSS9HEa2KGh4dmIprXt_XJircJ9SX4aimdb8zjDjs35B_YgRWXVmdZ6dgOMmyMY9koXEKcVq89kXEa7VujCdij-385iq8LmxLFCVx4FXw)
3. In a terminal that **has** been ssh’d into, open the file _/etc/hosts,_ typing \`sudo nano /etc/hosts\`. Similarly to step 1,  add a new line to the file and type \`\<yourcomputer\_ip\_address> \<yourcomputer\_hostname>\`. Save the changes. Your file should look like this: 

![](https://lh5.googleusercontent.com/Acc_m13lUw_-cliD2kZqw74V_lGdgYtMGp-Y1tFK08N65ozq6VtV1KCDlY3nl8kUW4DV8E2SoXZg-m6kwD8bEswu33UQorsdnLRii55TGZuj_PiKi5mV1ehkLRJCwJU9RJSNpnnNnzzol2uyrCjfbQ)

4. Now try running \`roslaunch astra\_camera astra.launch\` again to launch the camera. Hopefully, the issue should be resolved

\
\


✧･ﾟ: \*✧･ﾟ:\* A note about SSH! ✧･ﾟ: \*✧･ﾟ:\*

Once you have ssh’d into the turtlebot, you can run code that you have scp’d, just make sure you’re using the correct terminal where you’ve made the ssh connection. You can navigate within folders/directorie, list files (with the ‘ls’ command), move files around, and do all the things you could do if you were on the turtlebot physically using it through the command line. 


#### Debugging

If you try to run a file on your computer (NOT in the terminal you’ve ssh’d into) and you run into an error like the following:

![](https://lh6.googleusercontent.com/yxmV-GUAFV50xzKdC_LfXRy0NUdjfwPrmsh6dW7gq2hdE85L_OxViYVuZnSDiqRWc38EvNRq3ZskIdimg3F3rSF_HtnHX4FmxFCmk0qb28LUGLDIBHpAzAN26VyEUl51HEL2qxr3bysu5jDBV17IgA)

then print the ROS\_MASTER\_URI using the command \`echo $ROS\_MASTER\_URI\`. If you get a result that looks something like this:![](https://lh5.googleusercontent.com/pu6HtgV3GGzuX-mGJmAarcrKDy-XjXc_hiK5yIVu0FNhDa3HMUcPbvNPZk5ozZ-_8bxKEBDLKj-7Irzh23o-GCRzBhF798LkYxlPHBWd3_3Qr6mIIqaBATdb7HNbvCl0lWXUYrYPB1eOlBnOqOCjXA)

Then you’ll need to run the command \`export ROS\_MASTER\_URI=http\://\<turtlebot\_address>:11311\`:  ![](https://lh6.googleusercontent.com/nlXJxrL4MxL0o0w63_VhcHQWk21cBweOZnQaI-yAnNpRbhWy5hSrOfwsG65bXpTwG5Utl2aBsQ5fd5J95ZmjVGEFEpSpezqRWvlTDUtIZnAKfAexNjKMXzvMznaGFAEZhBiYExWNeIV42XXOKsBbMw)

Now try running the file again. It should be successful this time:![](https://lh3.googleusercontent.com/KArhnY7ilogfjttaP1AshW3VkGdeaXWKGxd_Fttv1zavxGnicYLdu1SDo3nUunKRzK_AEj4mKuVUTzc4IkfywZZ9BXsrNv5OL8H9EmB7Lkrv-59L5um7Uhagl-QhCbRLMqAjkv2LTzFBqBAEN67Hdg)

