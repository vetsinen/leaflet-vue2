<template>
  <l-map style="height: 300px" :zoom="zoom" :center="center">
    <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    <l-marker :lat-lng="markerLatLng"></l-marker>
  </l-map></template>

<script>
import L from 'leaflet';
import { LMap, LTileLayer, LMarker } from 'vue2-leaflet';

export default {
  name: "Map",
  data: function () {
    return {
      msg: 'hello, Leaflet',
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      attribution:
          '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      zoom: 15,
      center: [50.4536416,30.5227417],
      markerLatLng: [50.4536416,30.5227417]
    }
  },
  components: {
    LMap,
    LTileLayer,
    LMarker,
  },
}
</script>

<style scoped>

</style>