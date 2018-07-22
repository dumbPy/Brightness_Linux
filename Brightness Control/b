#!/usr/bin/python3

############################################################################################
#
# This script controls external monitor brightness using xrandr package.
#
############################################################################################ 


############################################################################################
# Directions to Use-

# Drop to root user .i.e., "sudo su" for Debian and Ubuntu.
# Copy this script to /usr/bin/ or any other system path.
# make the file executable by "chmod +x AbsolutePathTo/b"

# Now you can control brightness by "b DisplayNo. Brightness." 
# where, DisplayNo. starts with 1 and Brightness is generally between 0 and 1.
############################################################################################


############################################################################################ 
# eg. "b 1 0.7" to set brightness to 70% on 1st display.
############################################################################################



import os
import sys

#Get the attached displays
displays = os.popen("xrandr | grep ' connected ' | awk '{print$1 }'").read().split('\n')[:-1]

if (len(sys.argv)<3):
    print("Not Enough Arguments Passed \n")
    print("Try 'b <DisplayNo.> <Brightness>'\n\n")
    print("DisplayNo. Starts from 1 and Brightness varies from 0 to 1")
try:
    display = displays[int(sys.argv[1])-1]
    brightness = sys.argv[2]
    if(float(brightness)>1.5 or float(brightness) < 0):
        print("Brightness out of range. Try Between 0 and 1")
    else:
        os.system("xrandr --output "+display+" --brightness "+brightness)
    
except:
    print("Wrong Display Number. Choose from displays: "+ str(list(range(1, len(displays)+1))))
