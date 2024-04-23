<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title class="ion-text-center">Hediyeey</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content fullscreen>
      <swiper class="mySwiper" :options="swiperOptions">
        <swiper-slide v-for="(slide, index) in slides" :key="index">
          {{ slide }}
        </swiper-slide>
        <div class="swiper-pagination"></div> <!-- Pagination elementi -->
      </swiper>
    </ion-content>
  </ion-page>
</template>

<script setup>
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import { Swiper, SwiperSlide } from 'swiper/vue';

const swiperOptions = {
  pagination: { // pagination özelliğini tanımla
    el: '.swiper-pagination',
  },
};

const slides = ['Birinci Görsel', 'İkinci Görsel', 'Üçüncü Görsel', 'Dördüncü Görsel (altında next butonu olacak)'];
</script>

<style scoped>
    html,
    body {
      position: relative;
      height: 100%;
    }

    body {
      background: #eee;
      font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
      font-size: 14px;
      color: #000;
      margin: 0;
      padding: 0;
    }

    .swiper {
      width: 100%;
      height: 100%;
    }

    .swiper-slide {
      text-align: center;
      font-size: 18px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .swiper-slide img {
      display: block;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
</style>
