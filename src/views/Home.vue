<template>
  <section>
    <section id="showcase" style="background-color:#E9ECEF">
      <div class="container py-5">
        <div class="row bg-success justify-content-center" style>
          <h1 class="col-10 display-3 text-center">珍宝古萃 千年底蕴</h1>
          <p
            class="col-10 lead"
          >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Repudiandae beatae blanditiis fugit eligendi, cupiditate tempore sit autem ad quisquam perferendis assumenda iusto necessitatibus error porro reprehenderit aperiam qui culpa quaerat.</p>
          <form>
            <div class="form-row">
              <div class="col-4">
                <input class="form-control" type="text" placeholder="关键字" />
              </div>
              <div class="col-4">
                <input class="form-control" type="text" placeholder="年代" />
              </div>
              <div class="col-4">
                <input class="form-control" type="text" placeholder="类别" />
              </div>
            </div>
            <div class="form-row py-4">
              <div class="col">
                <button class="btn btn-info col">搜索</button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </section>
    <section class="container my-5">
      <LatestPosts></LatestPosts>
    </section>
    <!-- TODO: 加入font awesome 完成这个section -->
    <section class="container-fluid bg-info py-5 text-white">
      <div class="row">
        <div class="col col-md-4">
          <h4 class="text-center">aaa</h4>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. A officia tenetur aut, voluptas eligendi architecto unde ad. Molestias porro repellat laborum illum, aut quam dicta illo ipsa vitae, nesciunt sequi?</p>
        </div>
        <div class="col col-md-4">
          <h4 class="text-center">aaa</h4>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. A officia tenetur aut, voluptas eligendi architecto unde ad. Molestias porro repellat laborum illum, aut quam dicta illo ipsa vitae, nesciunt sequi?</p>
        </div>
        <div class="col col-md-4">
          <h4 class="text-center">aaa</h4>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. A officia tenetur aut, voluptas eligendi architecto unde ad. Molestias porro repellat laborum illum, aut quam dicta illo ipsa vitae, nesciunt sequi?</p>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
import LatestPosts from "../components/LatestPosts.vue";

export default {
  name: "home",
  components: {
    LatestPosts
  }
};
</script>
