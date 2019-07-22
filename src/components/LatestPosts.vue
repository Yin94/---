<template>
  <div class="row">
    <div class="col-12 text-center">
      <h2 class="display-4">新品上架</h2>
    </div>
    <div class="col-4">
      <ItemCard :item="ph"></ItemCard>
    </div>
    <div class="col-4">
      <ItemCard :item="ph"></ItemCard>
    </div>
    <div class="col-4">
      <ItemCard :item="ph"></ItemCard>
    </div>
  </div>
</template>

<script>
const ph = {
  id: 1,
  name: "青花瓷",
  year: "1908",
  img: require("../assets/home-inside-3.jpg"),
  postTime: "07/20/2018"
};
import ItemCard from "./ItemCard.vue";
export default {
  components: {
    ItemCard
  },
  data: function() {
    return {
      ph: ph
    };
  }
};
</script>