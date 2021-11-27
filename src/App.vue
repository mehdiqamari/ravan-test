<template>
  <div dir="rtl">
    <tset-box class="test-box" v-bind:a="listtoshow" />
    <paginision
      :page="curntpage"
      @next="curntpage += 1"
      @befor="curntpage -= 1"
     
    />
  </div>
</template>

<script>
import { a } from "./data.js";
import TsetBox from "./components/TestBox.vue";
import Paginision from "./components/pag.vue";
export default {
  components: {
    TsetBox,
    Paginision,
  },
  data() {
    return {
      a,
      curntpage: 1,
      itemperpage: 1,
    };
  },
  computed: {
    listtoshow() {
      return this.a.slice(
        (this.curntpage - 1) * this.itemperpage,
        this.curntpage * this.itemperpage
      )
    },
  },
};
</script>

<style  scoped>
body {
  background-image: url("assets/1.jpg");
    background-position: center;
  background-attachment: fixed;
  background-size: 100%px 100%px;
}
.test-box{
  margin-top: 100px;
  margin-right: 100px;
}
</style>