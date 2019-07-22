<template>
  <div class="card listing-preview">
    <img
      :src="item.img"
      @click="$router.push(`/item-detail/${item.id}`)"
      class="card-img-top"
      alt="Card image cap"
    />
    <div class="card-body">
      <h5
        class="card-title text-center"
        @click="$router.push(`/item-detail/${item.id}`)"
      >{{item.name}}</h5>
      <p
        class="card-text"
      >This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      <!-- TODO: 加入价格,年代, 分类,  -->
      <p class="card-text">
        <small class="text-muted">Posted on {{item.postTime}}</small>
      </p>
    </div>
  </div>
</template>
<script>
export default {
  props: ["item"]
};
</script>