<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1 - Level 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1 - Level 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <ExploreContainer name="Tab 1 - Level 1">
        <ion-button @click="redirectToLevel2"> LEVEL 2 </ion-button>
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

const redirectToLevel2 = () =>
  router.push({
    name: "tab1_level2",
  });
</script>
