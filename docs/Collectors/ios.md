---
layout: default
title: iOS
parent: Collectors
has_children: false
nav_order: 10
---


# [STCiOSXDataCollector](https://github.com/STCData/STCiOSXDataCollector)

iOS/OSX application that logs detected text, human poses, window manager information and user actions from built in web browser, terminal emulator, camera, and any other external application

ios app that tracks human in frame and voice as well as allows to input label on the hardware/onscreen keyboard and video
has mode for "depth hands logging" (turns off ar body mode)
records recognized voice text
v2 and audio 






## Browser

runs human recognition on videos 

### UI

 - Sidebar
  - open new tab address bar
  - open tabs, hierarchially, by origin
   - close with swipe
   - current tab is highlighted
  - show closed tabs button (recent history)
  - search in history
 - Current tab


logs tabs their history etc

## Screencast

Runs on both in app and system wide streaming (if enabled). Recognizes ui elements and user actions.

- PIP window
 -  displays whats being sent onto server
 -  uses buttons for adding timestamped data labels

## Camera view

- recognizes human body poses
- recognizes human hands poses

### UI

- Toggle recognition logging
   - toggle chatGPT response
- Toggle camera cast
   - toggle on device human body/in camera text recognition
- Toggle camera front/back
- Toggle system wide screencast
- Toggle in app screen cast
   - toggle on device text recognition

![video cast mp3](https://stcdata.github.io/STCiOSXDataCollector/UITestVideos/DataCollectorUITests.DataCollectorUITests.testNameJohn.mp4?width=390&height=844)



