University of Pennsylvania, ESE 5190 Final Project: Step Counter

    Team Walkman🚶‍♂️
    Group Members: Pan hao, Lihong Zhao and Xingjian Chen
    Tested on: 1. Lenovo Legion 5 Pro 16" Laptop, Intel Core i7-12700H， Windows11 
               2. MacBook Air (M1, 2020), macOS Ventura 13.0
               3. Lenovo Legion R9000P 2021 15.6"
               
# Overview

In this project, we build a steps counter to detect people’s daily walking by using the IMU and LCD screen.
加点东西

# Showcase

[![Demo_Step-Counter](https://res.cloudinary.com/marcomontalbano/image/upload/v1672286692/video_to_markdown/images/youtube--YtTOuhUdWrI-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/YtTOuhUdWrI "Demo_Step-Counter")
           
# Insttuctions

## Component

### Pico4ml_Board

<div align=center>
<img src="https://github.com/ryanhpan/ESE5190-Final-Project/blob/main/media/materials/arducam-pico4ml-tinyml-dev-kit.webp" width="700">  
</div>

## Block Diagrams

<div align=center>
<img src="https://github.com/ese5190-walkman/ese-5190_final_project/blob/main/media/design/block_diagram.png" width="800">  
</div>

- The IMU module detects the movement of the user and generates the data of acceleration of linear velocity and  angular velocity.
- The Filter Algorithms remove the high frequency noise from the raw data. 
- The Data Processor identifies the signal pattern of “walking”.
- The Program counts the amount of steps in a certain amount of time.
- LCD Screen shows the amount of steps on the screen.

## Descritption of RP2040 development enviroment

## Code

We found the code for Magic Wand and made some modifications based on it. We are now able to successfully read the IMU data from ICM20948 and get it to display on the LCD screen (LCD_st7735) which is used by PIO.

Also, following Dalton's advice, we tried to find a few fixed reference points based on the camera module but we observed that the array read by camera was strange and it was hard to extract the data from it and find a few points as coordinate points. So we gave up that idea. 

The code is [here](https://github.com/ese5190-walkman/ese-5190_final_project/tree/main/code/in-progress).

### Libraries
- [ICM20948](https://github.com/ese5190-walkman/ese-5190_final_project/tree/main/code/libraries/ICM20948)
- [LCD_st7735](https://github.com/ese5190-walkman/ese-5190_final_project/tree/main/code/libraries/LCD_st7735)
- [Arducam_hm01b0](https://github.com/ese5190-walkman/ese-5190_final_project/tree/main/code/libraries/Arducam_hm01b0)

# Narrative overview of project's development

## Midpoint Demo

<div align=center>
<img src="https://github.com/ryanhpan/ESE5190-Final-Project/blob/main/diagram/moving%20counter%20demo.gif" width="600">  
</div>

### Moving state

<div align=center>
<img src="https://github.com/ryanhpan/ESE5190-Final-Project/blob/main/diagram/moving%20state.png" width="800">  
</div>

### Stopping state

<div align=center>
<img src="https://github.com/ryanhpan/ESE5190-Final-Project/blob/main/diagram/stopping%20state.png" width="800">  
</div>

# Troubleshooting

- [Logs](https://github.com/ryanhpan/ESE5190-Final-Project/blob/main/media/troubleshooting/notes.txt)

# Reflections

## Advantages/Disadvantages

## Recommendation to future teams

## Other design approaches/components we might try next time

# Feature/Accomplishment we found particularly satisfying

# An explanation of the PIO part of the code

## The diagram of the overal logic

## Introduction to the RP2040 PIO module

## What makes RP2040 a unique asset for a microcontroller

# Team overview
- [Hao Pan](https://github.com/ryanhpan)
- [Lihong Zhao](https://github.com/lihzhao14)
- [Xingjian Chen](https://github.com/AndYmeisterrrrr)


