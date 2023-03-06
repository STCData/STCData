---
layout: default
---

# STCData
System for collecting data from mobile devices and machine learning on it



```mermaid
flowchart BT
  subgraph STCiOSXDataCollector
    direction TB
    c1(ML Recognizers)
    br>Browser]
    cam1>Camera]
    scr1>Screencast]
    br-->|tab info\nhtml\nrendered html\nuser actions|c1
    cam1-->|image|c1
    scr1-->|current frame\nApp info|c1
  end
  subgraph Linux
    direction TB
    c2(STCX11DataCollector)
    scr2>Screencast]
    scr2-->c2
  end
  subgraph Android 
    c3(STCDroneDataCollector)
  end
  subgraph Cloud
    sActual[(STCDataServer)]
  end
  
  s{{<i>schemaless\nAvro based\nREST/Websockets\nProtocol</i>}}
  
  s---|domain/schema agnostic\nrealtime data for ML|sActual
  
  c1-. hand, body poses\n recognized text in apps\nrecognized speech\screencast .-> s
  c3-. drone telemetry\n location\ndrone camera stream\nrecognized objects\nuser input .-> s
  c2-. screencast\nrecognized text\nuser input .-> s
```


## Server

### [STCDataServer](https://github.com/STCData/STCDataServer)

A server that receives stream of timestamped data with evolution-resistant scheme from mobile clients, stores it in database, provides APIs for using it in machine learning



## Collectors


### [STCX11DataCollector](https://github.com/STCData/STCX11DataCollector)

Linux X11 application that logs windowing information, screenshots and recognized text, user actions


### [STCDroneDataCollector](https://github.com/STCData/STCDroneDataCollector)

Android drone control application that logs telemetry, video stream, recognized objects on video stream, user actions


### [STCiOSXDataCollector](https://github.com/STCData/STCiOSXDataCollector)

iOS/OSX application that logs detected text, human poses, window manager information and user actions from built in web browser, terminal emulator, camera, and any other external application



![video cast mp3](https://stcdata.github.io/STCiOSXDataCollector/UITestVideos/DataCollectorUITests.DataCollectorUITests.testNameJohn.mp4?width=390&height=844)
<!-- ![video cast](https://stcdata.github.io/STCiOSXDataCollector/UITestVideos/DataCollectorUITests.DataCollectorUITests.testNameJohn.gif)
 -->
