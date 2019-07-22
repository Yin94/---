<template>
  <div>
    <div class="row">
      <div v-for="ele in itemList" :key="ele.id" class="my-3 col-md-6 col-lg-4 col-xl-3">
        <ItemCard :item="ele"></ItemCard>
      </div>
    </div>
    <Pagination @pageShift="pageJump" :currentPage="currentPage" :itemsCount="60" :pageSize="6"></Pagination>
  </div>
</template>

<script>
import Pagination from "./Pagination.vue";
import ItemCard from "./ItemCard.vue";
export default {
  props: ["itemList"],
  components: {
    Pagination,
    ItemCard
  },
  data: function() {
    return {
      currentPage: 1
    };
  },
  methods: {
    pageJump(targetPage) {
      console.log(targetPage);

      this.currentPage = targetPage;
    }
  }
};
</script>

<style scoped>
img,
h5 {
  cursor: pointer;
}
</style>
