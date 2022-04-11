<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Feed</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-card v-for="(item, index) in feed" :key="index">
        <ion-card-header>
          <ion-img :src="item.image" :alt="index"></ion-img>
          <ion-card-subtitle>{{item.city}}</ion-card-subtitle>
          <ion-card-title>{{item.type}}</ion-card-title>
          <ion-button size="small" color="tertiary">
            <ion-icon :icon="map" />
          </ion-button>
        </ion-card-header>
      </ion-card>
    </ion-content>
  </ion-page>
</template>

<script>
import { defineComponent } from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import { map } from 'ionicons/icons';

export default  defineComponent({
  name: 'Tab1Feed',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage },
  setup() {
    return {
      map
    }
  },
  data: () => ({
    feed: [
      {
        image: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/A_surfer_surfing_on_the_ocean_%28Unsplash%29.jpg/640px-A_surfer_surfing_on_the_ocean_%28Unsplash%29.jpg',
        city: 'Barranquilla, Colombia',
        type: 'Hueco'
      },
      {
        image: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/A_surfer_surfing_on_the_ocean_%28Unsplash%29.jpg/640px-A_surfer_surfing_on_the_ocean_%28Unsplash%29.jpg',
        city: 'Cartagena, Colombia',
        type: 'Calle mala'
      },
      {
        image: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/A_surfer_surfing_on_the_ocean_%28Unsplash%29.jpg/640px-A_surfer_surfing_on_the_ocean_%28Unsplash%29.jpg',
        city: 'Santa Marta, Colombia',
        type: 'Hueco'
      }
    ]
  })
});
</script>
