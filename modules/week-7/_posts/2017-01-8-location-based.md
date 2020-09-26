---
title: Location Based Example
module: 7
jotted: true
---

# Location Based Example


Try it live with this <a href="https://codepen.io/nicolocarpignoli/pen/MWwzyVP" target="_new">Codepen</a>. It retrieves your position and places a text near you.

Please follow these simple steps:

1. Create a new project with the following snippet, and change add-your-latitude and add-your-longitude with your latitude and longitude, without the <>.
2. Run it on a server
3. Activate GPS on your phone and navigate to the example URL
4. Look around. You should see the text looking at you, appearing in the requested position, even if you look around and move the phone.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>GeoAR.js demo</title>
    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-look-at-component@0.8.0/dist/aframe-look-at-component.min.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar-nft.js"></script>
  </head>

  <body style="margin: 0; overflow: hidden;">
    <a-scene
      vr-mode-ui="enabled: false"
      embedded
      arjs="sourceType: webcam; debugUIEnabled: false;"
    >
      <a-text
        value="This content will always face you."
        look-at="[gps-camera]"
        scale="120 120 120"
        gps-entity-place="latitude: <add-your-latitude>; longitude: <add-your-longitude>;"
      ></a-text>
      <a-camera gps-camera rotation-reader> </a-camera>
    </a-scene>
  </body>
</html>
```

<a href="https://ar-js-org.github.io/AR.js-Docs/" target="_new">Source</a>