<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no" />
  <title>Esri Leaflet</title>

  <!-- Load Leaflet from CDN -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
    integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
    crossorigin=""/>
  <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
    integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
    crossorigin=""></script>

  <!-- Load Esri Leaflet from CDN -->
  <script src="https://unpkg.com/esri-leaflet@3.0.0/dist/esri-leaflet.js"></script>
  <script src="https://unpkg.com/esri-leaflet-vector@3.0.0/dist/esri-leaflet-vector.js"></script>

  <style>
    body { margin:0; padding:0; }
    #map {
        position: absolute;
        top:0;
        bottom:0;
        right:0;
        left:0;
        font-family: Arial, Helvetica, sans-serif;
        font-size: 14px;
        color: #323232;
      }
  </style>

</head>

<body>
  <div id="map"></div>
  <script>

    const apiKey = "AAPK947bf115dd8d44da9b119d18ed465670bSQfPQOvMqOLYYWGprUm0df469-0wWWO27mnQPE11xqj1T5YtjdKxaYJkxN2hJST";
    const basemapEnum = "ArcGIS:Imagery";

    const map = L.map('map', {
      minZoom: 2
    }).setView([-30,0], 13);

    L.esri.Vector.vectorBasemapLayer(basemapEnum, {
      apiKey: apiKey
    }).addTo(map);

  </script>
</body>

</html>
