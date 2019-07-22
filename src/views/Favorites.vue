<template>
  <div>
    <section class="container-fluid bg-success text-white">
      <div class="row">
        <div class="col-12 text-center">
          <h1 class="display-4">收藏夹</h1>
          <p>
            <strong>李四</strong> 您好, 看看您喜欢的宝贝
          </p>
        </div>
      </div>
    </section>

    <FavList></FavList>
  </div>
</template>

<script>
import FavList from "../components/FavList.vue";
export default {
  data: function() {
    return {};
  },
  components: {
    FavList
  }
};
</script>