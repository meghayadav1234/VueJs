<template>
  <form v-on:submit="addItem">
    Name :
    <input type="text" v-model="name" />
    <button type="submit">Submit</button>
  </form>
</template>
<script>
export default {
  name: "AddItems",
  data() {
    return {
      name: ""
    };
  },
  methods: {
    addItem(e) {
      e.preventDefault();
      const newItem = {
        id: 4,
        name: this.name,
        marked: true
      };
      console.log(newItem);
      this.$emit("add-item", newItem);
      this.name = "";
    }
  }
};
</script>