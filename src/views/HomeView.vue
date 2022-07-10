<template>
  <home-banner/>
  <home-about/>
  <home-tech/>
  <faq-company/>
  <info-banner title="Support service for you" text="24/7 support
works for you seven days a week" to="/" :img="supportBannerImg"/>
  <partners-company/>
</template>
<script setup>
import HomeBanner from "../components/HomeBanner.vue";
import HomeAbout from "../components/HomeAbout.vue";
import HomeTech from "../components/HomeTech.vue";
import FaqCompany from "../components/FaqCompany.vue";
import InfoBanner from '../components/InfoBanner.vue'
import supportBannerImg from "../assets/images/support-banner.png";
import PartnersCompany from "../components/PartnersCompany.vue";</script>