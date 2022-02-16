<template>
  <div class="v-main-wrapper">
    <h3>CATALOG</h3>
    <vCatalog />
    <vCart />
  </div>
</template>

<script>
import vCatalog from "./v-catalog.vue";
import vCart from "./v-cart.vue";
export default {
  name: "v-main-wrapper",
  components: { vCatalog, vCart },
  props: {},
  data() {
    return {
      title: "Main wrapper",
    };
  },
  computed: {},
  methods: {},
  watch: {},
  mounted() {
    console.log("hello wrapper");
  },
};
</script>


<style scoped>
.v-main-wrapper {
  max-width: 900px;
  margin: 0 auto;
}
</style>