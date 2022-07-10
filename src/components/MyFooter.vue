<template>
  <footer class="footer">
    <div class="footer__block">
      <div class="footer__item">
        <my-logo :logo="logo"/>
        <div class="footer__copyright">Copyright © 2022 DubaiIt, Inc. All rights reserved.</div>
      </div>
      <div class="footer__item flex">
        <div class="footer__wrapper">
          <router-link class="footer__link" to="/">Cookies</router-link>
          <router-link class="footer__link" to="/">
            Privacy
          </router-link>
          <router-link class="footer__link" to="/">
            Terms
          </router-link>
        </div>
        <div class="footer__wrapper">
          <router-link class="footer__link" to="/">
            Continuity Policy
          </router-link>
          <router-link class="footer__link" to="/">Blog</router-link>
          <router-link class="footer__link" to="/">Clients</router-link>
        </div>
      </div>
      <div class="footer__wrapper">
        <a class="footer__link" href="tel:+7 (800) 555-35-35">+7 (800) 555-35-36</a>
        <a class="footer__link" href="mailto:example@pochta.com">example@pochta.com</a>
        <div class="flex <lg:block">
          <a href="/" class="footer__social">
            <img class="footer__icon" src="../assets/images/social/facebook.svg" alt="facebook">
          </a>
          <a href="/" class="footer__social">
            <img class="footer__icon" src="../assets/images/social/twitter.svg" alt="twitter">
          </a>
          <a href="/" class="footer__social">
            <img class="footer__icon" src="../assets/images/social/vk.svg" alt="vk">
          </a>
          <a href="/" class="footer__social">
            <img class="footer__icon" src="../assets/images/social/youtube.svg" alt="youtube">
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import MyLogo from "./MyLogo.vue";
import logo from "../assets/images/logo.png";</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.footer {
  background: rgba(51, 51, 51, 0.6);
  backdrop-filter: blur(10px);
  box-shadow: 0px 10px 20px 10px rgba(33, 177, 255, 0.2);
  @include fluid(padding-top, 30px, 60px);
  @include fluid(padding-bottom, 25px, 50px);

  &__block {
    @include container;
    display: flex;
    justify-content: space-between;
  }

  &__copyright {
    @include fluid(margin-top, 15px, 30px);
    @include fluid(font-size, 14px, 16px);
    font-weight: 400;
    color: $light;
  }

  &__wrapper {
    display: flex;
    flex-direction: column;
    @include fluid(margin-right, 100px, 215px);

    &:last-child {
      margin-right: 0;
    }
  }

  &__link {
    @include fluid(margin-bottom, 10px, 20px);
    @include fluid(font-size, 14px, 16px);
    color: #FFFFFF;
    opacity: 0.8;
    transition: $trn;

    &:last-child {
      margin-bottom: 0;
    }

    &:hover {
      opacity: 1;
    }
  }

  &__social {
    @include fluid(margin-right, 10px, 20px);
    @include fluid(width, 18px, 20px);
    @include fluid(height, 18px, 20px);

    &:last-child {
      margin-right: 0;
    }

    &:hover {
      .footer {
        &__icon {
          opacity: 1;
        }
      }
    }
  }

  &__icon {
    transition: $trn;
    opacity: 0.5;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
}

@media screen and (max-width: 992px) {
  .footer {
    &__block {
      flex-direction: column;
    }

    &__wrapper {
      margin-right: 30px;
    }

    &__item {
      margin-bottom: 30px;
    }

    &__social {
      margin-top: 15px;
      width: 25px;
      height: 25px;
      margin-right: 30px;
    }
  }
}
</style>