<template>
  <div class="about">
    <h1>This is {{Number(mode)?'Signin':'Signup'}} page</h1>
    <Form :mode="Number(mode)"></Form>
  </div>
</template>

<script>
import Form from "../components/AuthForm.vue";
export default {
  components: {
    Form
  },
  data: function() {
    return {
      mode: this.$route.params.mode
    };
  },
  watch: {
    $route(to, from) {
      this.mode = to.params["mode"];
    }
  }
};
</script>