---
title: AR Requirements
module: 7
jotted: false
---

# AR Requirements

## Import the library
AR.js from version 3 has a new structure.

AR.js is coming in two, different builds. They are both maintained. They are exclusive.

The file you want to import depends on what features you want, and also which render library you want to use (A-Frame or three.js).

AR.js uses jsartoolkit5 for tracking, but can display augmented content with either three.js or A-Frame.

You can import AR.js in one version of your choice, using the <script> tag on your HTML.

## AR.js with Image Tracking + Location Based AR

Import AFRAME version:

```html
<script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar-nft.js">
```

Import three.js version:

```html
<script src="https://raw.githack.com/AR-js-org/AR.js/master/three.js/build/ar-nft.js">
```

AR.js with Marker Tracking + Location Based AR:

Import AFRAME version:

```html
<script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js">
```

Import three.js version:

```html
<script src="https://raw.githack.com/AR-js-org/AR.js/master/three.js/build/ar.js">
```

If you want to import a specific version, you can do that easily replacing master with the version tag, e.g.:

```html
<script src="https://raw.githack.com/AR-js-org/AR.js/3.0.0/aframe/build/aframe-ar-nft.js">
```

### Requirements

Some requirements and known restrictions are listed below:

1. It works on every phone with webgl and webrtc.
2. Marker based is very lightweight, while Image Tracking is more CPU consuming
3. You cannot use Chrome on iOS, as Chrome on iOS did not support, at the moment, camera access
4. On device with multi-cameras, Chrome may have problems on detecting the right one. Please use Firefox if you find that AR.js opens on the wrong camera. There is an open issue for this.
5. To work with Location Based feature, your phone needs to have GPS sensors
6. Please, read carefully any suggestions that AR.js pops-up -as alerts- for Location Based on iOS, as iOS requires user actions to activate geoposition
Location Based feature is only available on A-Frame
7. Always deploy under https
8. Accessing to the phone camera or to camera GPS sensors, due to major browsers restrictions, can be done only under https websites.

All the examples you will see, and all AR.js web apps in general, have to be run on a server. You can use local server or deploy the static web app on the web.

So don't forget to always run your examples on secure connections servers or localhost. **Github Pages** is a great way to have free and live websites under https.

<a href="https://ar-js-org.github.io/AR.js-Docs/" target="_new">Source</a>