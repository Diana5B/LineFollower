# ROBOTICS HACKATHON (20.01.2024) - Line Follower
A twelve-hour line follower hackathon serves as the concluding project for the third-year Introduction to Robotics course

### Task:
#### The objective is for the robot to precisely track the line, aiming for the most accurate performance to complete the course. The robot is allowed three attempts to achieve the fastest time.

Team: Powerpuff Girls
- [@lemnaruamedeea](https://github.com/lemnaruamedeea)
- [@vfranci](https://github.com/vfranci)

Best time: 17.871

<details>
  <summary>
      <h2>Electronic Setup</h2>
  </summary>
  <br>

  Components:
- Arduino Uno
- Power source: LiPo battery
- Two wheels
- QTR-8A reflectance sensor
- Ball caster
- L293D motor driver
- Two DC motors
- Medium breadboard
- Wires (M - F, M - M), zip-ties, screws as needed

## Project and Design Description
  For the chassis we cut into a foam board after measuring an apropriate distance between the wheels and for the sensor. Zip-ties were employed to fasten the breadboard and battery, while we utilized additional zip-ties to secure the Arduino board and motors in place.

  ### Requirements
Minimum requirements for the project were to have the robot finish the line follower track, including the curved lines. To achieve maximum grade, the course had to be finished in under 20 seconds and, upon starting, the sensor had to be calibrated using automatic motor movement.

### Driver Connection table
![driver](https://github.com/Diana5B/IntroductionToRobotics/assets/115624763/6ff3e419-10f6-4da1-8ee2-fd11d2852a0a)
![dreiverconectoins](https://github.com/Diana5B/IntroductionToRobotics/assets/115624763/6354afb0-ffa4-4bb5-8aad-238afbf29b6a)

### Motors and Sensor Connection scheme
![conections](https://github.com/Diana5B/IntroductionToRobotics/assets/115624763/13678f93-3829-4d93-b855-fa69145b2a28)


  </br>
  </details>


  <details>
  <summary>
      <h2>Software implementation</h2>
  </summary>
  <br>

  The robot calibrated its sensor by moving left and right in order to recognize the black line it had to follow. The movement behaviour was determined by using a proportional-integrative-derivative controller. We started with a simple code provided by our teacher in which we had to alter the kp, ki, and kd values to achieve the desired movement. We started by assigning random values to the proportional constant in order to observe the behaviour. Once the robot was able to take the turns without overshooting, we began updating the kd value to smooth the wobble.

  The final values were:
- kp = 4.3;
- ki = 0.000;
- kd = 23.2;

Afterwards, we implemented the automatic calibration and juggled the tresholds for the error and motor speed values.

  </br>
  </details>

 ### [Code](https://github.com/Diana5B/LineFollower/blob/main/Line.ino)
 
 ### Final Track:
### ![track](https://github.com/Diana5B/IntroductionToRobotics/assets/115624763/174339b1-8565-4157-9866-2e1dbc4f5054)

 ### Final setup of the robot: 
### ![Robot](https://github.com/vfranci/Line-Follower/assets/115077321/08085af5-6bf5-4b55-920f-c0e0b4081a76)

 ### Watch the robot on the circuit:
 ### [Video](https://youtu.be/-rcJyTiLDLg?si=OaZJrGN7fROQkyiY)
