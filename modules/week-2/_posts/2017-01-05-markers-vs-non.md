---
title: AR Markers
module: 2
---


# What are AR Markers

<div class="tab">
  <button class="tablinks" onclick="openTab(event, 'Markers')">Markers</button>
  <button class="tablinks" onclick="openTab(event, 'Non')">Non-Markers</button>
</div>

<div id="Markers" class="tabcontent" style="display:block">
<p>
Marker – Augmented Reality
People talking about augmented reality often mention the words “tracking” and "markers". But what are augmented reality markers? In this article, we want to give you a short explanation and a few examples of existing markers.
In short: Augmented reality markers or short AR-markers are visual cues which trigger the display of the virtual information.  Markers are normal images or small objects which are trained beforehand so that they can be recognized later in the camera stream.  After a marker is recognized, its position, scale, and rotation are derived from visual cues and transferred to the virtual information. At this point let us give you a few examples of the most common markers.

</p>
<table>
<tr><td colspan="3">Frame Marker</td></tr>
<tr>
<td><img src="AR_Toolkit_Marker.png" width="100" height="100" /></td>
<td><img src="Vuforia_Marker.png" width="100" height="100" /></td>
<td><img src="csm_Bild_02_2050c79c00.jpg" width="100" height="100" /></td>
</tr>
</table>

<p>Real-time recognition of rectangles in pictures has been perfected over the years. Even if they rotated or skewed. That’s why it’s no surprise that the first marker is a border marker. A Border marker is usually a 2D-image which is printed on a piece of paper or another smooth surface. These markers are square and got a significant black ( sometimes white ) border. During the tracking phase, the system searches for a black rectangle. Only if it found one it examines the interior of the border to determine the real marker. Depending on how the border ís skewed the system can extract the position and rotation of the marker in relation to the camera.</p>

<a href="https://anymotion.com/en/wissensgrundlagen/augmented-reality-marker#:~:text=Marker%20%E2%80%93%20Augmented%20Reality&text=In%20short%3A%20Augmented%20reality%20markers,later%20in%20the%20camera%20stream." target="_new"><em>Reference</em></a>

</div>

<div id="Non" class="tabcontent" style="display:block">
<p>
</p>
</div>
