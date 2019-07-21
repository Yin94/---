<template>
  <div>
    <div class="row">
      <div v-for="ele in itemList" :key="ele.id" class="my-3 col-md-6 col-lg-4 col-xl-3">
        <div class="card listing-preview">
          <img
            :src="ele.img"
            @click="$emit('clicked', ele.id)"
            class="card-img-top"
            alt="Card image cap"
          />
          <div class="card-body">
            <h5 class="card-title" @click="$emit('clicked', id)">{{ele.name}}</h5>
            <p
              class="card-text"
            >This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
            <!-- TODO: 加入价格,年代, 分类,  -->
            <p class="card-text">
              <small class="text-muted">Posted on {{ele.postTime}}</small>
            </p>
          </div>
        </div>
      </div>
    </div>
    <Pagination @pageShift="pageJump" :currentPage="currentPage" :itemsCount="60" :pageSize="6"></Pagination>
  </div>
</template>

<script>
import Pagination from "./Pagination.vue";
export default {
  props: ["itemList"],
  components: {
    Pagination
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
