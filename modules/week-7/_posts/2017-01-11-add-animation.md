---
title: Add animation
module: 7
jotted: true
---

# Add animation

What if we wanted to add animation to our object?

```html

<!doctype HTML>
<html>
    <script src="https://aframe.io/releases/0.8.0/aframe.min.js"></script>

    <script src="https://cdn.rawgit.com/jeromeetienne/AR.js/1.5.5/aframe/build/aframe-ar.js"></script>

    <script src="https://rawgit.com/donmccurdy/aframe-extras/master/dist/aframe-extras.loaders.min.js"></script>

    <body style='margin : 0px; overflow: hidden;'>
        <a-scene embedded arjs='sourceType: webcam; debugUIEnabled: false; detectionMode: mono_and_matrix; matrixCodeType: 3x3;'>
            <a-marker preset="hiro">
                <a-entity>
                    <a-animation attribute="rotation"
                    dur="2000"
                    easing="linear"
                    from="0 0 0"
                    to="0 360 0"
                    repeat="indefinite"></a-animation>
                    <a-entity rotation="0 0 25">
                        <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
                        <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
                        <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
                        <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
                        <a-sky color="#ECECEC"></a-sky>
                    </a-entity>
                </a-entity>
            </a-marker>
        <a-entity camera></a-entity>
        </a-scene>
    </body>
</html>

```