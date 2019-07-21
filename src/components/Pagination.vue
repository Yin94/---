<template>
  <nav aria-label="Page navigation example">
    <ul class="pagination">
      <li @click="pageJump(-1)" :class="liClass(1)">
        <router-link class="page-link" to="#" aria-label="Previous">
          <span aria-hidden="true">&laquo;</span>
          <span class="sr-only">Previous</span>
        </router-link>
      </li>
      <li v-for="i in pageCount" @click="pageJump(i-currentPage)" :class="liClass(i)" :key="i">
        <router-link class="page-link" to="#">{{i}}</router-link>
      </li>
      <li @click="pageJump(1)" :class="liClass(pageCount)">
        <router-link class="page-link" to="#" aria-label="Next">
          <span aria-hidden="true">&raquo;</span>
          <span class="sr-only">Next</span>
        </router-link>
      </li>
    </ul>
  </nav>
</template>
<script>
export default {
  props: ["itemsCount", "pageSize", "currentPage"],
  computed: {
    pageCount: function(props) {
      return Math.ceil(props.itemsCount / props.pageSize);
    }
  },
  methods: {
    liClass(i) {
      return i === this.$props.currentPage ? "page-item disabled" : "page-item";
    },
    pageJump(opt) {
      const pageToBe = this.$props.currentPage + opt;
      if (
        pageToBe === this.$props.currentPage ||
        pageToBe < 1 ||
        pageToBe > this.pageCount
      )
        return;
      this.$emit("pageShift", pageToBe);
    }
  }
};
</script>

<style scoped>
li.disabled {
  cursor: not-allowed;
}
</style>
