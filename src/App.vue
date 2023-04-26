<template>
  <div
    style="
      display: flex;
      width: 100%;
      height: 100vh;
      justify-content: center;
      align-items: center;
    "
  >
    <div style="height: 900px; width: 1600px">
      <l-map
        :options="{ attributionControl: false }"
        :useGlobalLeaflet="false"
        ref="map"
        v-model:zoom="zoom"
        :center="[47.41322, -1.219482]"
      >
        <l-tile-layer
          url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
          layer-type="base"
          name="OpenStreetMap"
        ></l-tile-layer>
      </l-map>
    </div>
  </div>
</template>

<script>
import "leaflet/dist/leaflet.css";
import { LMap, LTileLayer } from "@vue-leaflet/vue-leaflet";

export default {
  components: {
    LMap,
    LTileLayer,
  },
  data() {
    return {
      zoom: 2,
    };
  },
};
</script>

<style></style>

