---
layout: default
title: World Map
nav_order: 2
---

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<script src='https://api.mapbox.com/mapbox.js/plugins/leaflet-fullscreen/v1.0.1/Leaflet.fullscreen.min.js'></script>
<link href='https://api.mapbox.com/mapbox.js/plugins/leaflet-fullscreen/v1.0.1/leaflet.fullscreen.css' rel='stylesheet' />

<style>
  #ttrpg-map {
    height: 75vh;
    width: 100%;
    border: 2px solid #333;
    background: #1a1a1a;
    z-index: 1;
  }

  @media (max-width: 600px) {
    #ttrpg-map {
      height: 60vh;
    }
  }
</style>

<div id="ttrpg-map"></div>

<script>
  // 1. Setup the map for a "Simple" coordinate system (non-geographic)
  var map = L.map('ttrpg-map', {
    crs: L.CRS.Simple,
    minZoom: -2
    trackResize: true
  });

  // 2. Define the dimensions of your hand-drawn image
  var w = 2000, // Replace with your image width
      h = 1500, // Replace with your image height
      url = '{{ "/assets/images/twg-regional-map.jpg" | relative_url }}';

  // 3. Map the image coordinates
  var southWest = map.unproject([0, h], map.getMaxZoom()-1);
  var northEast = map.unproject([w, 0], map.getMaxZoom()-1);
  var bounds = new L.LatLngBounds(southWest, northEast);

  // 4. Add the image to the map
  L.imageOverlay(url, bounds).addTo(map);

  // 5. Tell the map to fit the image
  map.setMaxBounds(bounds);
  map.fitBounds(bounds);

  // Responsive Resize Listener
  window.addEventListener('resize', function() {
    map.invalidateSize();
    map.fitBounds(bounds);
  });

// TEMPORARY COORDINATE FINDER
map.on('click', function(e) {
    var coords = map.project(e.latlng, map.getMaxZoom()-1);
    var x = Math.round(coords.x);
    var y = Math.round(coords.y);
    
    // This creates a popup exactly where you clicked showing the coordinates
    L.popup()
        .setLatLng(e.latlng)
        .setContent("X: " + x + "<br>Y: " + y)
        .openOn(map);
        
    // It also logs it to the console (F12) for easy copying
    console.log("Coordinate: [ " + x + ", " + y + " ]");
});

  // 6. ADDING MARKERS (This is where the magic happens)
  // Format: L.marker(map.unproject([x, y], map.getMaxZoom()-1))
  var rockchester = L.marker(map.unproject([500, 800], map.getMaxZoom()-1)).addTo(map);
  rockchester.bindPopup("....<a href='...' target='_blank'>Discover this location</a>");

</script>