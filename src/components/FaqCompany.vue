<template>
  <div class="faq">
    <my-title title="FAQ"/>
    <n-collapse arrow-placement="right">
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="1">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae!
          Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="2">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aperiam aspernatur commodi deleniti
          ducimus, et fuga libero minus vero voluptas. Consequuntur cum, facere nisi obcaecati quis recusandae sint vel?
          Ipsam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="3">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae!
          Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="4">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aperiam aspernatur commodi deleniti
          ducimus, et fuga libero minus vero voluptas. Consequuntur cum, facere nisi obcaecati quis recusandae sint vel?
          Ipsam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="5">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="6">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aperiam aspernatur commodi deleniti
          ducimus, et fuga libero minus vero voluptas. Consequuntur cum, facere nisi obcaecati quis recusandae sint vel?
          Ipsam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="7">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae!
          Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
      <n-collapse-item title="Lorem ipsum dolor sit amet, consectetur adipisicing elit?" name="8">
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aperiam aspernatur commodi deleniti
          ducimus, et fuga libero minus vero voluptas. Consequuntur cum, facere nisi obcaecati quis recusandae sint vel?
          Ipsam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis harum minus quod vitae! Architecto,
          asperiores, aspernatur assumenda dolorem eligendi esse est in, iusto laborum quam quas quia sint voluptates.
          Blanditiis.
        </div>
      </n-collapse-item>
    </n-collapse>
  </div>
</template>

<script setup>
import MyTitle from "./MyTitle.vue";</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins.scss';

.faq {
  @include container;
  @include fluid(margin-bottom, 25px, 50px);
}

</style>