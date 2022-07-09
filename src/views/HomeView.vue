<template>
  <home-banner/>
  <home-about/>
  <home-tech/>
  <faq-company/>
  <info-banner title="Мы всегда рядом" text="Круглосуточная поддержка
работает для вас без выходных" to="/" :img="supportBannerImg"/>
</template>
<script setup>
import HomeBanner from "../components/HomeBanner.vue";
import HomeAbout from "../components/HomeAbout.vue";
import HomeTech from "../components/HomeTech.vue";
import FaqCompany from "../components/FaqCompany.vue";
import InfoBanner from '../components/InfoBanner.vue'
import supportBannerImg from "../assets/images/support-banner.png";</script>