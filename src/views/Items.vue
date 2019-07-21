<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <div class="container">
        <h1 class="display-4">古今中外 瓷器之家</h1>
        <p
          class="lead"
        >This is a modified jumbotron that occupies the entire horizontal space of its parent.</p>
      </div>
    </div>
    <div class="container">
      <ItemList @clicked="clickedHandler" :itemList="itemList"></ItemList>
    </div>
  </div>
</template>

<script>
import ItemList from "../components/ItemList.vue";
export default {
  components: {
    ItemList
  },
  data: function() {
    return {
      itemList: Array(8).fill({
        id: 1,
        name: "青花瓷",
        year: "1908",
        img: require("../assets/home-inside-3.jpg"),
        postTime: "07/20/2018"
      })
    };
  },
  methods: {
    clickedHandler(id) {
      this.$router.push(`/item-detail/${id}`);
    }
  }
};
</script>

