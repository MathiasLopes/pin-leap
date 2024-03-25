<template>
  <ion-content fullscreen>
    <div id="map" style="height: 100%;"></div>
  </ion-content>
</template>

<script>
import { defineComponent, onMounted } from 'vue';
import { IonContent } from '@ionic/vue';
import * as L from 'leaflet';
import 'leaflet/dist/leaflet.css';

export default defineComponent({
  name: 'Map',
  components: {
    IonContent
  },
  setup() {
    onMounted(() => {
      const map = L.map('map').setView([51.505, -0.09], 13);

      L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; OpenStreetMap contributors'
      }).addTo(map);
    });
  }
});
</script>

<style scoped>
#map {
  height: 100%;
}
</style>
