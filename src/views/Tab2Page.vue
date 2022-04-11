<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Nuevo</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      
      

    </ion-content>
  </ion-page>
</template>

<script>
import { defineComponent } from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';

export default defineComponent({
  name: 'Tab2Nuevo',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
});
</script>
