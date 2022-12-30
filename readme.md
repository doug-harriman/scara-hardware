# SCARA Robot Arm

## Description

Learning project to build a SCARA robotic arm.  

Design elements targeted for learning in this project:

* Mechanical design elements
    * SolidWorks
    * Personally fabricating as many parts as feasible.
    * Robust bearing system
        * Custom bearing races and cage
    * Single stage cycloidal drive with very low backlash
        * Ball bearings in cycloidal
    * 3 digit gripper
        * 2 fingers + 1 thumb
        * Fingers move towards each other as they approach the thumb.  Allows for flat & round gripping
        * Force controlled not position controlled.
        * Capstan tendon drive.
        * +/- 180 degree rotation
        * Vertical travel

* Electronics 
    * KiCAD
    * Custom FOC driver board 

* Algorithmic
    * BLDC motors with FOC control
        * Custom FOC firmware
    * OpenModelica Model
        * Controller development against model
    * MIMO control with feedback linearization
    * Cartesian trajectory input file via G-Code
        * Multi-segment lookahead with jerk limited profiles
    * Vision system integration for item pick & place
        * ML based object recognition
    * ROS integration
        * ROS simulation

## Design Phases

1. Basic Arm - Simple 2 axis mechanism
    1. Direct drive axes
        1. Motor bearings for joint bearings
    1. Static base
    1. BLDC driver dev board
        1. Custom FOC firmware
        1. Board per axis
    1. Master board
    1. No gripper
    1. Simple pen up/down to demonstrate basic motion control

1. Gripper

1. Joint Mechanics R2
    1. Joint bearings external to motor
    1. Cycloidal gear box