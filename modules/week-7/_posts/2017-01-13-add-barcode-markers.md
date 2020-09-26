---
title: Add Custom Markers
module: 7
jotted: true
---

# Add Custom Markers

What if we want to add custom Markers?

```html

<!doctype HTML>
<html>
    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
  <!-- we import arjs version without NFT but with marker + location based support -->
  <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
    <body style='margin : 0px; overflow: hidden;'>
        <a-scene embedded
         arjs="detectionMode: mono_and_matrix; matrixCodeType: 4x4_BCH_13_9_3;">
    <!-- marker id=0 -->
    <a-marker type="barcode" value="0">
        <a-sphere material="color: blue; opacity: 0.5" radius="0.25"></a-sphere>
    </a-marker>

    <!-- marker id=1 -->
    <a-marker type="barcode" value="1">
        <a-text value="Detected id:1"></a-text>
    </a-marker>

    <a-entity camera></a-entity>
</a-scene>
    </body>
</html>
```

Use these <a href="https://github.com/nicolocarpignoli/artoolkit-barcode-markers-collection" target="_new">barcodes</a>.

