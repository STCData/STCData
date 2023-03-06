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
      “onScreenData” on document with object { screenData: pixelBuffer, textRecognizer: {boxes: [ {x, y, width, height, “recognized text in box1”}, {x, y, width, height, “recognized text in box2” }…]}}. Note that the only way to receive a screen data is to subscribe to this event
    Following functions are already attached to document object:
      submitLabel(label: String, callback: (error)->void)
    User prompt: “place a half transparent button over each recognized box of text. When user click on it, show a dropdown with options: good, bad, average. When label is submitted show alert”
    Output separately minified html of div#content, css and js like that
    😳HTML
    ```
    (Only div#content and its children)
    ```
    🧐JS
    ```
    (JS without any comments, prettified)
    ```
    😎CSS
    ```
    (Minified css)
    ```

    Do not output any explanations!





    modify previous response according to user prompt. output only modified lines in DIFF format with line numbers, inside of 
    😳HTML
    ```
    html diff goes here
    ```
    🧐JS
    ```
    js diff goes here
    ```
    😎CSS
    ```
    css diff goes here
    ```
    as needed.
    user prompt is: "make buttons blue, barely visible, with corner radius 0.4"
    Do not output any explanations!
