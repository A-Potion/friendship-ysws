 <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
     integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY="
     crossorigin=""/>

 <script>
     import { onMount } from 'svelte';
     
     onMount(() => {
         const script = document.createElement('script');
         script.src = 'https://unpkg.com/leaflet@1.9.4/dist/leaflet.js';
         script.integrity = 'sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=';
         script.crossOrigin = 'anonymous';
         script.onload = () => {
             const map = window.L.map('map').setView([35.9045, -79.0469], 5);

             window.L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
                 maxZoom: 19,
                 attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
             }).addTo(map);
         };
         document.head.appendChild(script);
     });

 </script>

<style>
    #map { height: 100vh; }
</style>

<div id="map"></div>

