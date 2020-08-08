---
title: AR Markers
module: 2
---


# What are AR Markers

<div class="tab">
  <button class="tablinks" onclick="openTab(event, 'Overview')">Overview</button>
<button class="tablinks" onclick="openTab(event, 'Frame')">Frame Markers</button>
<button class="tablinks" onclick="openTab(event, 'Image')">Image/NFT Markers</button>
</div>

<div id="Overview" class="tabcontent" style="display:block">
<p>
People talking about augmented reality often mention the words "tracking" and "markers". But what are augmented reality markers? In this article, we want to give you a short explanation and a few examples of existing markers.
</p>
<p>In short: Augmented reality markers or short AR-markers are visual cues which trigger the display of the virtual information.  Markers are normal images or small objects which are trained beforehand so that they can be recognized later in the camera stream.  After a marker is recognized, its position, scale, and rotation are derived from visual cues and transferred to the virtual information. At this point let us give you a few examples of the most common markers.
</p>
</div>

<div id="Frame" class="tabcontent">

<table>
<tr>
<td><img src="../imgs/AR_Toolkit_Marker.png" width="100" height="100" /></td>
<td><img src="../imgs/Vuforia_Marker.png" width="100" height="100" /></td>
<td><img src="../imgs/csm_Bild_02_2050c79c00.jpg" width="100" height="100" /></td>
</tr>
</table>

<p>Real-time recognition of rectangles in pictures has been perfected over the years. Even if they rotated or skewed. That’s why it’s no surprise that the first marker is a border marker. A Border marker is usually a 2D-image which is printed on a piece of paper or another smooth surface. These markers are square and got a significant black ( sometimes white ) border. During the tracking phase, the system searches for a black rectangle. Only if it found one it examines the interior of the border to determine the real marker. Depending on how the border ís skewed the system can extract the position and rotation of the marker in relation to the camera.</p>

</div>

<div id="Image" class="tabcontent">
<table>
<tr>
<td><img src="../imgs/AugementedRealityMarkerAnymotion.jpg" width="100" height="100" /><br />Initial Image</td>
<td><img src="../imgs/AugementedRealityMarkerAnymotionFeatures.jpg" width="100" height="100" /><br />Natural Image</td>
<td><img src="../imgs/ImEinsatz.jpg" width="100" height="100" /><br />In action</td>
</tr>
</table>
<p>Known under a few names we think NFT or natural feature Tracking Marker is the most appropriate name. NFT markers are the next logical step to framemarkers. NFT markers are images too but you don’t need the black border anymore. Instead, you extract so-called natural features from any picture you like. The problem is to determine “good” natural features and up to this point, it is much more trial and error than when using a frame marker. Every AR-frameworks has his own little secrets in this regard and quality and stability varies greatly from framework to framework.</p>

</div>
<div id="GPS" class="tabcontent">
<table>
<tr>
<td><img src="../imgs/POI.jpg" width="100" height="100" /><br />POI</td>
<td><img src="../imgs/Garmin.jpg" width="100" height="100" /><br />Web Video</td>
<td><img src="../imgs/Pokemon.jpg" width="100" height="100" /><br />Pokemon</td>
</tr>
</table>
<p>Using one’s gps position as a marker would be the first idea most people have. You could give objects, for example, a model of a building , it’s own gps coordinate and display it relative to your position. The reason why this is hardly done is the inaccuracy of this method. Depending on the gps hardware objects can appear up to 5 meters from their designated positions. Despite this shortcoming, there are a few applications which use gps markers because they don’t need high accuracy.  On example is an app which shows you the approximate direction of pois ( points of interest ). Another example is the computation of your current speed based on your gps coordinates over a certain time.</p>
<p>Some people would mention the map of the popular game Pokemon Go at this point. But although we got a gps marker and virtual additional information, it is disputable if this is really AR since the “reality” part of “augmented reality” is missing. Both the gps marker and the additional information are displayed on the virtual google map. If anything else this would qualify as augmented virtuality.</p>

<p>Advancement in hard- and software lead to new approaches in this area but in most cases, developers combine gps marker with some other method.</p>
</div>

<a href="https://anymotion.com/en/wissensgrundlagen/augmented-reality-marker#:~:text=Marker%20%E2%80%93%20Augmented%20Reality&text=In%20short%3A%20Augmented%20reality%20markers,later%20in%20the%20camera%20stream." target="_new"><em>Reference</em></a>