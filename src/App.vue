<template>
  <div>
      <tset-box v-bind:a="a"/>
          
  </div>
</template>

<script>
import { a } from "./data.js";
import TsetBox from "./components/TestBox.vue";
export default {
  components: {
    TsetBox,
  },
  data() {
    return {
      a
    }
  },
};
</script>

<style>
body{
    background-image: url("assets/1.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-attachment: fixed;
    background-size: 100%px 100%px;
}
</style>