<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
       <ion-buttons slot="start">
        <!-- Geri butonu için router-link -->
        <router-link to="/tabs/tab1">
       <ion-icon :icon="chevronBack" color="primary" size="large"></ion-icon>
      </router-link>
     </ion-buttons>
    <ion-title>Favories</ion-title>
   </ion-toolbar>
  </ion-header>

      <ExploreContainer name="Tab 3 page" />
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import { chevronBack,  } from 'ionicons/icons';

</script>
