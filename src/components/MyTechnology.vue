<template>
  <my-title title="Our services" />
  <div class="container">
    <div class="card" v-motion-pop-visible>
      <div class="card__flex">
        <div class="card__item">
          <div class="card__title">Template site</div>
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service1.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            A template site is suitable for those who want to get a site quickly
            enough or very cheaply. The main advantage of such sites is the
            built-in adaptability, and the main disadvantage is that it is quite
            difficult to make changes to the template other than changing texts,
            pictures and colors of buttons and panels.
          </div>
          <div class="card__cost">Prise 500$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__flex">
        <div class="card__item">
          <div class="card__title">Landing page</div>
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service2.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            The main goal of a one-pager is to get a high conversion: around 5%
            from paid traffic. Conversion is the ratio of the number of users
            who left a request or called to the total number of website
            visitors.
          </div>
          <div class="card__cost">prise 750$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__flex">
        <div class="card__item">
          <div class="card__title">Chatbot</div>
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service3.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            Messenger marketing is gaining more and more popularity these days.
            86% of mobile phone users have at least one of the messengers: Whats
            App, Viber, Skype, Telegram.
          </div>
          <div class="card__cost">500$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__flex">
        <div class="card__item">
          <div class="card__title">Mobile app</div>
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service4.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            In the modern world, the concept of creating a mobile application
            without creating a website is very relevant. This will be especially
            true for those who provide their customers with some kind of
            service.
          </div>
          <div class="card__cost">prise 250$</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import MyTitle from "./MyTitle.vue";
</script>
<style scoped lang="scss">
@import "../assets/styles/mixins.scss";
.container {
  @include container();
  display: flex;

  flex-wrap: wrap;
}
.card {
  @include fluid(padding-top, 10px, 20px);
  @include fluid(padding-bottom, 10px, 20px);
  @include fluid(padding-right, 20px, 40px);
  @include fluid(padding-left, 20px, 40px);
  transition: $trn;
  border-radius: 15px;
  width: 46%;
  margin-right: 8%;
  margin-bottom: 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid $light;

  &:nth-child(2n) {
    margin-right: 0;
  }
  &__flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  &__item {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 48%;
  }
  &__cost {
    @include fluid(font-size, 14px, 16px);
    @include fluid(margin-top, 10px, 15px);
    color: #fff;
    text-transform: uppercase;
    font-weight: 500;
  }
  &__title {
    @include fluid(font-size, 14px, 18px);
    @include fluid(margin-bottom, 10px, 20px);
    color: #fff;
    text-transform: uppercase;
    font-weight: 600;
  }
  &__text {
    text-align: center;
  }
  &__img {
    width: 100%;
    height: 200px;
    @include fluid(margin-top, 10px, 20px);
    @include fluid(margin-bottom, 10px, 20px);
    object-fit: contain;
    border-radius: 15px;
  }
}
</style>
