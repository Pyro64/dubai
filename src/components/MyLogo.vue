<template>
  <a href="#banner">
    <img :src="logo" alt="logo"/>
  </a>

</template>

<script setup>
const props = defineProps({
  logo: String
});
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

img {
  @include fluid(width, 40px, 55px);
  @include fluid(height, 40px, 55px);
  object-fit: contain;
}
</style>
