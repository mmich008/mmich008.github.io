---
Header: "Maps"
layout: page
title: Maps
description: Different maps of Palestine
background: '/img/dmMap.jpg'
---

<html>
<head>
<meta charset='utf-8' />
<title>Display a map</title>
<meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.53.0/mapbox-gl.js'></script>
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.53.0/mapbox-gl.css' rel='stylesheet' />
<style>
body { margin:0; padding:0; }
#map { position:absolute; top:0; bottom:0; width:100%; }
</style>
</head>
<body>

<div id='map'></div>
<script>
mapboxgl.accessToken =  'pk.eyJ1IjoibWFyeW1pY2hhZWwiLCJhIjoiY2pyaDFkcXh2MnFkazRhbW11cGltNmlseCJ9.SORv6TYY8vs480ZDrDFvrg';
const map = new mapboxgl.Map({
container: 'map',
style: 'mapbox://styles/marymichael/cjtkh4jyq0am91flqv0nex5va',
center: [34.474008, 31.518104],
zoom: 11.6
});
</script>

</body>
</html>
