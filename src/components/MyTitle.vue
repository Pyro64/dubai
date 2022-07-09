<template>
  <div class="title">{{ title }}</div>
</template>

<script setup>
const props = defineProps({
  title: String
})
</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.title {
  @include fluid(font-size, 24px, 36px);
  font-weight: 600;
  position: relative;
  text-align: center;
  width: fit-content;
  margin: auto;
  @include fluid(margin-bottom, 25px, 50px);

  &::before {
    content: "";
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    transition: $trn;
    background: $light;
    width: 100%;
    border-radius: 3px;
    @include fluid(bottom, -5px, -10px);
    @include fluid(height, 2px, 3px);
  }
}
</style>