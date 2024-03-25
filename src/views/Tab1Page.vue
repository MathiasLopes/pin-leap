<script setup lang="ts">
  import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonSearchbar } from '@ionic/vue';
  import Map from '@/components/Map.vue';

  var animated:boolean = true;

</script>

<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Lieux</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-searchbar autocapitalize="" :animated=animated ></ion-searchbar>
      <Map></Map>
    </ion-content>
  </ion-page>
</template>

<style>

#map {
  height:100%;
}

</style>