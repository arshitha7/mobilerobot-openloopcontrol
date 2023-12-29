# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Take the Ep core robot insert the battery and check the battery percentage


Step2:

Turn on the robot and connect the robot to the computer through WIFI

Step3:

 Open visual studio and import robomaster package and do all the code



Step4:

Take the measurement of the track on each and every turn and gives the values trhough code in (m)

Step5:

Run the program to see the roboto movement

## Program
```
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    ep_chassis.move(x=2.3, y=0, z=0, xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
    ep_chassis.move(x=0.5, y=0, z=70, xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x=0.9, y=0, z=80, xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
    ep_chassis.move(x=0.9, y=0, z=30, xy_speed=1.3).wait_for_completed()
    
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
    ep_chassis.move(x=0.7, y=0, z=0, xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")
    ep_chassis.move(x=0, y=0, z=50).wait_for_completed()
    
    ep_led.set_led(comp = "all",r=204,g=153,b=255,effect="on")
    ep_chassis.move(x=0, y=1.5, z=0, xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")
    ep_chassis.move(x=0, y=0, z=135).wait_for_completed()

    ep_led.set_led(comp = "all",r=102,g=102,b=153,effect="on")
    ep_chassis.move(x=-1.5, y=0, z=0,xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
    ep_chassis.move(x=0, y=0, z=-85).wait_for_completed()

    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")
    ep_chassis.move(x=2, y=0, z=0,xy_speed=1.3).wait_for_completed()
    
    ep_led.set_led(comp = "all",r=255,g=204,b=153,effect="on")
    ep_chassis.move(x=0, y=0, z=80,xy_speed=1.3).wait_for_completed()
    
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=0.55, y=0, z=0,xy_speed=1.3).wait_for_completed()
    
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=0, y=0, z=0,xy_speed=1.3).wait_for_completed()

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![WhatsApp Image 2023-12-29 at 17 51 47_2c44101b](https://github.com/Raji1009/mobilerobot-openloopcontrol/assets/89059861/c8b6acd6-917b-40ec-8c08-5546a49fbeab)


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:
https://youtu.be/5k9NR2ovO20?si=R64RWAJO0A9smbig
## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
