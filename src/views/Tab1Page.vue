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

      <ExploreContainer name="Tab 1 page">
        <ion-button @click="redirectToLevel1"> LEVEL 1 </ion-button>
      </ExploreContainer>
    </ion-content>
  </ion-page>
</template>

<script lang="ts" setup>
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
  IonButton,
  useIonRouter,
} from "@ionic/vue";
import ExploreContainer from "@/components/ExploreContainer.vue";

const router = useIonRouter();

const redirectToLevel1 = () =>
  router.push({
    name: "tab1_level1",
  });
</script>
