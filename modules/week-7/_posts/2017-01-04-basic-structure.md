---
title: Basic Structure
module: 7
jotted: true
---

# Basic Structure of AR.js

This is main parts needed

```html
<!doctype HTML>
<html>

    <script src="https://aframe.io/releases/0.8.0/aframe.min.js"></script>

    <script src="https://cdn.rawgit.com/jeromeetienne/AR.js/1.5.5/aframe/build/aframe-ar.js"></script>

    <script src="https://rawgit.com/donmccurdy/aframe-extras/master/dist/aframe-extras.loaders.min.js"></script>

    <body style='margin : 0px; overflow: hidden;'>
        <a-scene embedded arjs='sourceType: webcam; debugUIEnabled: false; detectionMode: mono_and_matrix; matrixCodeType: 3x3;'>
            <a-marker preset="hiro">
                <a-box position='0 0.5 0' color="red"></a-box>-->
            </a-marker>
            <a-entity camera></a-entity>
        </a-scene>
  </body>
</html>

```