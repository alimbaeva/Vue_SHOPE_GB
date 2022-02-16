<template>
  <div class="v-catalog-item">
    <img
      class="v-catalog-item__image"
      :src="require('../assets/images/' + product_data.image)"
      alt="img"
    />
    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__price">Price: {{ product_data.price }} P</p>
    <button class="v-catalog-item__addBtn btn" @click="sendToParents">
      Add to card
    </button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {
    sendToParents() {
      this.$emit("sendArticle", this.product_data.article);
    },
  },
};
</script>

<style lang="scss">
.v-catalog-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 rgb(231, 171, 171);
  padding: 16px;
  margin-bottom: 16px;

  // &__image {
  //   width: 100px;
  // }
}
</style>