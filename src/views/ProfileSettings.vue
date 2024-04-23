<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-buttons slot="start">
            <!-- Geri butonu için router-link -->
            <router-link to="/tabs/tab4">
              <ion-icon :icon="chevronBack" color="primary" size="large"></ion-icon>
            </router-link>
          </ion-buttons>
          <ion-title>Settings</ion-title>
        </ion-toolbar>
      </ion-header>
  
      <ion-content color="light">
        <ion-list :inset="true">
          <!-- Settings düğmesi -->
          <router-link to="/tabs/settings" class="no-underline">
            <ion-item :button="true">
              <ion-icon color="danger" slot="start" :icon="shareOutline" size="large"></ion-icon>
              <ion-label>Share App</ion-label>
            </ion-item>
          </router-link>
  
          <!-- Upgrade düğmesi -->
          <ion-item :button="true">
            <ion-icon color="warning" slot="start" :icon="readerSharp" size="large"></ion-icon>
            <ion-label>Terms</ion-label>
            <ion-note slot="end"></ion-note>
          </ion-item>

          <ion-item :button="true">
            <ion-icon color="warning" slot="start" :icon="lockClosedOutline" size="large"></ion-icon>
            <ion-label>Privacy</ion-label>
            <ion-note slot="end"></ion-note>
          </ion-item>

          <ion-item :button="true">
            <ion-icon color="warning" slot="start" :icon="help" size="large"></ion-icon>
            <ion-label>Help</ion-label>
            <ion-note slot="end"></ion-note>
          </ion-item>


        </ion-list>
      </ion-content>
    </ion-page>
  </template>
  
  <script setup lang="ts">
  import { IonPage, IonToolbar, IonTitle, IonContent, IonButtons, IonItem, IonLabel, IonNote, IonIcon } from '@ionic/vue';
  import { chevronBack,  help,  lockClosedOutline,  readerSharp,  shareOutline } from 'ionicons/icons';
  </script>
  
  <style>
  /* no-underline sınıfı ile router-link'in alt çizgisini kaldırın */
  .no-underline {
    text-decoration: none;
  }
  </style>
  