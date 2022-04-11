<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="feed" href="/tabs/tab1">
          <ion-icon :icon="gridOutline" />
          <ion-label>Feed</ion-label>
        </ion-tab-button>
          
        <ion-tab-button tab="new" href="/tabs/tab2">
          <ion-icon :icon="addCircleOutline" />
          <ion-label>Nuevo</ion-label>
        </ion-tab-button>
        
        <ion-tab-button tab="settings" href="/tabs/tab3">
          <ion-icon :icon="personCircleOutline" />
          <ion-label>Settings</ion-label>
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script>
import { defineComponent } from 'vue';
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonPage, IonRouterOutlet } from '@ionic/vue';
import { personCircleOutline, gridOutline, addCircleOutline } from 'ionicons/icons';

export default defineComponent({
  name: 'TabsPage',
  components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage, IonRouterOutlet },
  setup() {
    return {
      gridOutline,
      personCircleOutline,
      addCircleOutline
    }
  }
});
</script>
