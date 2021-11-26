<template>
  <div>
    <div class="MinBox" v-for="i in a" :key="i.id" dir="rtl">
      <br>
      <div>{{i.titel}}</div>
      <div>{{i.a}}</div>
      <div>{{i.b}}</div>
      <div>{{i.c}}</div>
      <div>{{i.d}}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["a"]
};
</script>

<style>
.MinBox {
  background-color: rgb(245, 245, 245);
  height: 500px;
  width: 700px;
  border-radius: 8px;
  background-color: rgb(246, 247, 248);
  box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px,
    rgba(0, 0, 0, 0.3) 0px 30px 60px -30px;
}
.MinBox div {
  margin: 30px 16px 0px 25px;
}
</style>