<template>
  <nav>
    <a class="navlink" href="#about">About</a>
    <a class="navlink" href="#tech">Technologies</a>
    <a class="navlink" href="#faq">FAQ</a>
    <a class="navlink" href="#companies">Companies</a>
  </nav>
</template>

<script setup>
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

nav {
  @include fluid(margin-right, 30px, 60px);
}

.navlink {
  @include fluid(font-size, 14px, 16px);
  @include fluid(margin-right, 20px, 40px);
  position: relative;
  font-weight: 500;
  transition: $trn;
  color: $light;

  &:hover {
    color: $primary;

    &::after {
      width: 50%;
      opacity: 0.7;
    }
  }

  &::after {
    content: "";
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    transition: $trn;
    background: $primary;
    width: 0;
    border-radius: 3px;
    @include fluid(bottom, -5px, -10px);
    @include fluid(height, 2px, 3px);
  }

  &:last-child {
    margin-right: 0;
  }
}

.router-link-exact-active {
  &::after {
    width: 50%;
  }
}

@media screen and (max-width: 768px) {
  nav {
    margin-right: 0;
    width: 650px;
  }
}
</style>
