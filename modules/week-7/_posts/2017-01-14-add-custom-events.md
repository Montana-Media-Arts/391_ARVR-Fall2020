---
title: Add Custom Events
module: 7
jotted: true
---

# Add Custom Events

## Interaction with Overlayed DOM content

You can add interations by adding DOM HTML elements on the body. For example, starting from this example:

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

We can add on the body, outside the a-scene:

```html
<div class="buttons">
  <button class="say-hi-button"></button>
</div>
```

Then, we need to add some CSS to absolute positioning the DIV and BUTTON, and also some scripting to listen to click events.

You can customize your a-scene or content, like 3D models, play video, and so on. See on A-Frame Docs on how to change entity properties and work with events: https://aframe.io/docs/1.0.0/introduction/javascript-events-dom-apis.html.

We will end up with the following code:

```html
<!DOCTYPE html>
<html>
  <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
  <!-- we import arjs version without NFT but with marker + location based support -->
  <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
  <script>
    window.onload = function () {
      document
        .querySelector(".say-hi-button")
        .addEventListener("click", function () {
          // here you can change also a-scene or a-entity properties, like
          // changing your 3D model source, size, position and so on
          // or you can just open links, trigger actions...
          alert("Hi there!");
        });
    };
  </script>
  <style>
    .buttons {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 5em;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 10;
    }

    .say-hi-button {
      padding: 0.25em;
      border-radius: 4px;
      border: none;
      background: white;
      color: black;
      width: 4em;
      height: 2em;
    }
  </style>
  <body style="margin : 0px; overflow: hidden;">
    <div class="buttons">
      <button class="say-hi-button">SAY HI!</button>
    </div>
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

<a href="https://ar-js-org.github.io/AR.js-Docs/ui-events/" target="_new">Source</a>
