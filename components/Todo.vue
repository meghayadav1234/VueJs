<template>
  <div>
    <h1>{{message}}</h1>
    <h1>{{msg}}</h1>
  </div>
</template>
<script>
export default {
  name: "Todo",
  data() {
    return {
      message: "Hi"
    };
  },
  props: ["msg"]
};
</script>
<style scoped>
</style>