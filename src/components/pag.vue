<template>
  <div>
    <button v-if="page > 1 " v-on:click="gotobefor">قبلی</button>
    <button v-if="page < 30" v-on:click="gotonext">بعدی</button>
  </div>
</template>

<script>
export default {
  props: {
    page: {
      type: Number,
      required: true,
    },
  },
  methods: {
    gotonext() {
      this.$emit("next");
    },
    gotobefor() {
      this.$emit("befor");
    },
  },
};
</script>

<style scoped>
button {
  height: 60px;
  width: 150px;
  background-color: rgb(180, 246, 204);
  border: none;
  border-radius: 5px;
  margin: 50px 50px 50px 50px;
}
</style>