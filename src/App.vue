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
</style>