<template>
  <my-title title="Our services" />
  <div class="container">
    <div class="card" v-motion-pop-visible>
      <div class="card__title">CRM system for organization</div>
      <div class="card__flex">
        <div class="card__item">
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service1.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            CRM systems help businesses optimize processes by streamlining
            mundane workloads, enabling employees to focus on creative and more
            high-level tasks. Lead management. Sales leads can be tracked
            through CRM, enabling sales teams to input, track and analyze data
            for leads in one place. Human resource management (HRM).
          </div>
          <div class="card__cost">Priсe from 30 000$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__title">automatic operation with Data science</div>

      <div class="card__flex">
        <div class="card__item">
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service2.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            A data science driven organization can be described as an entity
            that maximizes the value from the data available while using machine
            learning and analytics to create a sustainable competitive
            advantage.
          </div>
          <div class="card__cost">Priсe from 150 000$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__title">artificial intelligence based OPEN AI</div>

      <div class="card__flex">
        <div class="card__item">
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service3.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            Artificial intelligence is based on the principle that human
            intelligence can be defined in a way that a machine can easily mimic
            it and execute tasks, from the most simple to those that are even
            more complex. The goals of artificial intelligence include mimicking
            human cognitive activity.
          </div>
          <div class="card__cost">Priсe from 130 000$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__title">Mobile app</div>

      <div class="card__flex">
        <div class="card__item">
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
          <div class="card__cost">Priсe from 50 000$</div>
        </div>
      </div>
    </div>
    <div class="card" v-motion-pop-visible>
      <div class="card__title">Designing and Production</div>

      <div class="card__flex">
        <div class="card__item">
          <img
            class="card__img"
            alt="img"
            src="../assets/images/service5.png"
          />
        </div>
        <div class="card__item">
          <div class="card__text">
            Designing and Production of software that manage and optimize energy
            consumption and commercial generation for private houses, airports,
            machinery, malls.
          </div>
          <div class="card__cost">Priсe from 50 000$</div>
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
  @include fluid(margin-bottom, 50px, 100px);
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
  &:last-child {
    margin: auto;
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
    height: 100%;
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
    object-fit: contain;
    border-radius: 15px;
  }
}

@media screen and(max-width: 992px) {
  .card {
    width: 100%;
    margin-right: 0;
  }
}

@media screen and(max-width: 576px) {
  .card {
    &__flex {
      flex-direction: column;
    }

    &__item {
      width: 100%;
    }
  }
}
</style>
