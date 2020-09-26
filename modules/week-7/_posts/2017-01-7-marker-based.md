---
title: Marker Based Example
module: 7
jotted: true
---

# Marker Based Example

Please follow these simple steps:

1. Create a new project with the code below (or open this <a href="https://ar-js-org.github.io/AR.js/aframe/examples/marker-based/basic.html" target="_new">live example</a> and go directly to the last step)
2. Run it on a server
3. Open the website on your phone
4. Scan this <a href="../imgs/hiro.png" target="_new">picture</a> to see content through the camera.

```html
<!DOCTYPE html>
<html>
  <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
  <!-- we import arjs version without NFT but with marker + location based support -->
  <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
  <body style="margin : 0px; overflow: hidden;">
    <a-scene embedded arjs>
      <a-marker preset="hiro">
        <a-entity
          position="0 0 0"
          scale="0.05 0.05 0.05"
          gltf-model="https://arjs-cors-proxy.herokuapp.com/https://raw.githack.com/AR-js-org/AR.js/master/aframe/examples/image-tracking/nft/trex/scene.gltf"
        ></a-entity>
      </a-marker>
      <a-entity camera></a-entity>
    </a-scene>
  </body>
</html>
```

<a href="https://ar-js-org.github.io/AR.js-Docs/" target="_new">Source</a>