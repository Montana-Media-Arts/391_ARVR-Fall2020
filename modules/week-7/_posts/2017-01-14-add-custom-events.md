---
title: Add Custom Markers
module: 7
jotted: true
---

# Add Custom Events

What if we want to add custom Events?

```html

<!doctype HTML>
<html>
    <script src="https://aframe.io/releases/0.8.0/aframe.min.js"></script>
    <script src="https://cdn.rawgit.com/jeromeetienne/AR.js/1.5.5/aframe/build/aframe-ar.js"></script>
    <script src="https://rawgit.com/donmccurdy/aframe-extras/master/dist/aframe-extras.loaders.min.js"></script>

    <script>
    // create custom events
    
    </script>
    <body style='margin : 0px; overflow: hidden;'>
        <a-scene embedded arjs='sourceType: webcam; debugUIEnabled: false; detectionMode: mono_and_matrix; matrixCodeType: 3x3;'>
            <a-marker preset="hiro"> 

                <a-gltf-model src="https://raw.githubusercontent.com/KhronosGroup/glTF-Sample-Models/master/2.0/AnimatedMorphSphere/glTF/AnimatedMorphSphere.gltf"></a-gltf-model>

            </a-marker>
            <a-entity camera></a-entity>
        </a-scene>
    </body>
</html>
```