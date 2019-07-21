<template>
  <div class="container">
    <div class="row">
      <div class="col-md-9" style>
        <img :src="require('../assets/home-1.jpg')" style="max-width:100%" />
        <div class="row thumbs m-2">
          <div class="col-3" v-for="ele in item.imgs" :key="ele">
            <a href="#">
              <img class="img-fluid" :src="ele" :alt="ele" />
            </a>
          </div>
        </div>
      </div>
      <div class="col-md-3 desc-card">
        <h2>{{item.name}}</h2>
        <h3>{{item.year}}</h3>
        <div class="collapse-group">
          <p>
            You need to keep your enterprise secure, and you want to do it on your terms.
            <span
              class="collapse"
              id="viewdetails"
            >{{item.desc}}</span>
            <a data-toggle="collapse" style="color:#307DF6" data-target="#viewdetails">
              <strong>More... &raquo;</strong>
            </a>
          </p>
        </div>
        <div class="row justify-content-around">
          <button class="col-md-5 btn btn-primary">联系卖家</button>
          <button class="col-md-5 btn btn-success">加入收藏</button>
        </div>
      </div>
    </div>
  </div>
  <!-- TODO: use lightbox modal -->
</template>


<script>
export default {
  // props: ["item"],
  data: function(props) {
    return {
      item: {
        name: "元青花",
        year: "1993",
        imgs: [
          require("../assets/home-1.jpg"),
          require("../assets/home-inside-3.jpg")
        ],
        desc:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores sit cupiditate asperiores cumque quia vitae molestias vero itaque debitis optio! Provident facere temporibus quibusdam voluptatibus dicta sequi asperiores sapiente rerum?"
      }
    };
  }
};
</script>


<style scoped>
a:hover {
  filter: brightness(80%);
}
</style>
