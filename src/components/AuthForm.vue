<template>
  <form action>
    <input type="text" value="username" />
    <input type="text" value="password" />
    <template v-if="!mode">
      <input type="text" value="username" />
      <input type="text" value="password" />
    </template>
    <!-- TODO:add boostrap  -->
  </form>
</template>

<script>
import { log } from "util";
export default {
  props: ["mode"],
  data: function(props) {
    return {};
  }
};
</script>