<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>
    <ion-button @click="setRouteQuery">set route param</ion-button>
      <ExploreContainer name="Tab 1 page" />
    </ion-content>
  </ion-page>
</template>

<script>
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButton, modalController } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import Modal from '@/components/modal.vue';
export default  {
  name: 'Tab1',
  components: { ExploreContainer, IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonButton },
  methods: {
    setRouteQuery() {
      const queryParam = {
        workshopdirectory: 'test',
        workshopid: 'test2',
        title: 'test3',
      };
      this.$router.push({ query: queryParam });
    },
  }
}
</script>