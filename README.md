# Size-based Object Marking and Segregation
[![License MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://github.com/Prasheel24/object-marking-segregation/blob/master/License)
---

## Author
Prasheel Renkuntla - [GitHub](https://github.com/Prasheel24)

I am pursuing my Master's in Robotics at the University of Maryland, College Park. My primary area of interest is in Vision integrated Robot Systems.

## Overview
* This project demonstrates the use of 7 Degrees of Freedom of a KUKA LBR4 iiwa R820 arm.
* The aim of this project is to mark and segregate objects (pick and place) on a conveyor belt based on its size.
* The project is simulated in CoppeliaSim and DH table verified in MATLAB.

## Motivation
Each product undergoes rigorous testing before it is launched into the market.  For a food manufacturing plant, each stage from raw material to final product is tested carefully. When an undesired incident occurs in a testing facility i.e, a hazardous event that can affect the personnel working which consequently stops the food production then, with the use of a robot arm can overcome the problem. The arm maneuvers through its workspace doing the processes that humans can do without being damaged. Such a safe environment can help both the personnel and the company producing the product. Hence, to visualise this scenario, a 7 DoF serial link manipulator is used to complete the tasks in a testing facility setting. The arm here will use a gripper to pick an object.  Based on the object size, the arm will take it to the corresponding sprayer to get painted, and place it accordingly on a table. Using the mathematical  model that we know, we  will define the motion of the object to do such a process. With this defined model, we will simulate a robot arm with a gripper to validate the kinematic and contact model.

## Applications 
This model shows that the arm can pick, color and place an object efficiently in its
workspace. Following are some applications where this arm can be used-
* Chemical testing
* Product Packaging
* Food manufacturing plant

General applications include -
* Collaborative Robots
* Machine Trending
* Material Handling

## Assumptions
In order to define the kinematic model of the robot manipulator, the following assumptions were made -
* Objects of interest are rigid with high friction coefficient.
These  objects  (containers  in  a  chemical  lab)  are  rigid  dynamic  bodies.   Friction coefficient is high as the gripper will be able to hold it steady.
* Objects are placed in fixed locations.
The arm can position itself near these objects to pick and place at certain positions. Hence, no sensing modelling is defined as the object locations are known.
* Painting modifier will run only when the object is in front of it.
* No path planning for the arm.
The object locations are fixed and placed in its workspace carefully. Hence, there is no path planning done on the arm to avoid these obstacles.
* Kinematics of the model are considered.
The dynamics of the arm are neglected as the arm is allowed to move with a very low velocity and acceleration. 

## Dependencies
* MATLAB - [Installation](https://www.mathworks.com/downloads/)
* CoppeliaSim - [Installation](http://coppeliarobotics.com/downloads)

## Run
* To run the simulation, use this file - [ProjectFinal](https://github.com/Prasheel24/object-marking-segregation/tree/master/code/ProjectFinal.ttt)
* Check A Matrices(DH table) from Forward Kinematics, open this file - [ProjectValidation](https://github.com/Prasheel24/object-marking-segregation/tree/master/code/ProjectValidation.m)

## Demo
The setup in which robot arm works is shown below - 
<p align="center">
<h5>Simulation Environment</h5>
<img src="/output/setup.PNG" width="70%">
</p>
The simulation will show the usage of arm workspace. The sprayer needs to be configured on each run for a specific color. Below figure shows the object being sprayed black.
<p align="center">
<h5>Object Sprayed</h5>
<img src="/output/sprayed.PNG" width="70%">
</p>
The conveyor has three different sized objects. Based on this size, the robot arm will pick each of the three objects to its specific sprayer. Post the sprayer action completion, the arm will place the object on the table nearby. When the task is complete, the robot arm will go back to its initial configuration.
<p align="center">
<h5>Completed Task</h5>
<img src="/output/completed.PNG" width="70%">
</p>

## License 
```
MIT License

Copyright (c) 2020 Prasheel Renkuntla

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
## References
* Kuka LBR4 iiwa R820 - [Documentation](https://www.kuka.com/-/media/kuka-downloads/imported/9cb8e311bfd744b4b0eab25ca883f6d3/kuka_lbr_iiwa_brochure_en.pdf?rev=5a25f7eac825492e92af6343dbf5bc6b)
* RG2 Gripper - [Documentation](https://www.universal-robots.com/media/1226143/rg2-datasheet-v14.pdf)
* Kinematics and Contact Modelling- [Book](https://www.cds.caltech.edu/~murray/books/MLS/pdf/mls94-complete.pdf)
* CoppeliaSim - [Documentation](http://www.coppeliarobotics.com/helpFiles/)
