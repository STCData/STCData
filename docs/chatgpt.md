---
layout: default
title: ChatGPT Enabled
parent: Features
nav_order: 1
has_children: false
---


a prompt for ChatGPT that enables it respond on "Overlay green boxes over humans you see on the screen": 
"write a js code that will be run in CombineWebView with dimensions 768x1388. underneath it you user can see a human 
figure, code that you will write can receive the coordinates of the recognized
hands as an array with objects with format: {x:, y:} on js event "received labeled data"




    analyze user's prompt and output relevant to it json in following format.
    {“enabledSources”:  array of enum Camera, Screen
           “enabledPipelines:  array of enum HandRecognizer, HumanBodyRecognizer, TextRecognizer, CatRecognizer
           “webviewTag” enum CameraOverlay, BrowserOverlay, PiPView, SideBarTop, SideBarBottom}
    user prompt: "place a button to picture in picture, on its bottom, when user clicks it - save all text"
    do not output any explanations!


    Write a code in JavaScript, that’s being executed in environment where following events are being emitted:
      “onScreenData” with object { “screenData”: pixelBuffer, “textRecognizer”: { [ {x, y, width, height, “recognized text in box1”}, {x, y, width, height, “recognized text in box2”}… ] }. Note that the only way to receive a screen data is to subscribe to this event
    Following function is available:
      submitLabel(label: String, callback: (error)->void)
    Browser window where this JS code is run is placed directly on top of the screen, and resolution of browser and screen are matched.
    User prompt: “place a half transparent button over each recognized box of text. When user click on it, show a dropdown with options: good, bad, average. When label is submitted show alert”
    Output separately minified html of div#content, css and js like that
    😳HTML
    ```
    (Only div#content and its children)
    ```
    🧐JS
    ```
    (JS without any comments)
    ```
    😎CSS
    ```
    (Minified css)
    ```

    Do not output any explanations!
