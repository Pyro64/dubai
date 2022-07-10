<template>
  <div class="case">
    <my-title title="How we can help you"/>
  </div>
</template>

<script setup>
import MyTitle from "./MyTitle.vue";</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.case {
  @include container;
}
</style>