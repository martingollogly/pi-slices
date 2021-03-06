# Pi Remote CAR

This is a DIY project for a Pi Car hobbyist (estimated build time)

## Step 1: Get a Chassis and Build it (2-4 hours)

Remote Car usin Sain smart chassis and can be bought on Amazon or SainSmart website http://www.sainsmart.com/ for about £6

### Before

<img src="https://images-na.ssl-images-amazon.com/images/I/61qH18xAjVL._SL1200_.jpg" height="340" >

### After

<img src="pi-car-chassis-wired.jpg" height="340" >

## Step 2: Wire up (2-4 hours)

Hook up to a motor board to control the wheels. 

Starting with the a breadboard to write the motor functions (with design from fritzing)

<img src="raspberry-pi-connect-motor-board.png" height="240" >

See https://javatutorial.net/raspberry-pi-control-motor-speed
See https://www.youtube.com/watch?v=LwEBB6v559I

## Step 3: Connect Pi and other sensors

TODO Hook up a Pi Zero to control as main processing unit and control of other cars components 

## Step 4: Add camera and Web interface

The following is the best link I've come across and comes complete with Web interface and configuration screen for camera. 
```
  git clone https://github.com/silvanmelchior/RPi_Cam_Web_Interface.git
  cd RPi_Cam_Web_Interface
  chmod u+x *.sh
  ./install.sh
  ```
  
## Step 5: Add Sensors for Collision avoidance

The following is the best link I've come across. 

  https://www.modmypi.com/blog/hc-sr04-ultrasonic-range-sensor-on-the-raspberry-pi

> Note: I've tried this out and currently it's partially working but the sensor readings are not consistent and need some debugging

 ``` 
   cd distance_sensor
   chmod +x distanct.py
   sudo python distance.py
 
  ```
  
### TODO: 
* Add loop to keep sending distane
* Add condition to only register when threshold is reached (e.g. 10 cms)
* Test with multiple sensors and refactor code

## Step 6,7,8 TODO 
* Add Tensorflow for AI and image recongnition
* Add Web Interface for Movement

  https://github.com/fivdi/pigpio
* Add Temperature Sensors to follow heat signatures
