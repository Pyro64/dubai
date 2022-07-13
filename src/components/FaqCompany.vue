<template>
  <div class="faq">
    <my-title title="FAQ" />
    <n-collapse arrow-placement="right">
      <n-collapse-item
        title="
How do we help businesses?"
        name="1"
      >
        <div>
          Web development services refer to building, creating, and maintaining
          websites, it includes services like web design, web development, and
          database management. Choosing the right web development partner for
          your project is always crucial, especially when it comes to building a
          successful product. We have years of experience and a proven record of
          delivering complex web apps solutions.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Who is a designer?" name="2">
        <div>
          UX/UI designers aim to build interfaces that are easy and pleasant to
          use and also look perfect. The job of this team member is to adjust to
          the visual aspect of the project as well as make sure that the visual
          and interactive aspects of your app are easy to get for a potential
          user.
        </div>
      </n-collapse-item>
      <n-collapse-item
        title="
Why us?"
        name="3"
      >
        <div>
          We do our best and offer alternative solutions rather than just going
          with the flow and accepting what is given to us.
        </div>
      </n-collapse-item>
      <n-collapse-item
        title="Mobile app development for startups & enterprises"
        name="4"
      >
        <div>
          We develop smart mobile apps of various kinds and size – from small
          MVPs to mobile layers working on top of complex systems.
        </div>
      </n-collapse-item>
      <n-collapse-item
        title="
Enterprise Software Development "
        name="5"
      >
        <div>
          Leverage our expertise in enterprise software development, API
          integration, modernising legacy systems, and consolidating app
          portfolios. We help large organizations become a lasting success in
          the global arena by re-engineering solutions of different complexity.
        </div>
      </n-collapse-item>
      <n-collapse-item
        title="
Dedicated Development Team"
        name="6"
      >
        <div>
          Scale your delivery capacity with intelligent dedicated developers.
          Our clients succeed by leveraging process of building, motivating, and
          managing software development teams.
        </div>
      </n-collapse-item>
      <n-collapse-item
        title="
IT Consulting services "
        name="7"
      >
        <div>
          Use the expertise and deep tech background of the best minds at
          Intellectsoft to create a comprehensive IT strategy for a digital and
          technological transformation of your organization that goes in line
          with your business objectives. Our strategic IT consulting will help
          you automate and digitalise operations, optimise the software
          portfolio, and implement the latest technologies.
        </div>
      </n-collapse-item>
    </n-collapse>
  </div>
</template>

<script setup>
import MyTitle from "./MyTitle.vue";
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

.faq {
  @include container;
  @include fluid(margin-bottom, 25px, 50px);
}
</style>
