<template>
  <div id="app">
    <todo msg="Welcome" />
    <AddItems v-on:add-item="add" />
    <ShowItems v-bind:itemLists="itemList" />
  </div>
</template>

<script>
import Todo from "./components/Todo.vue";
import ShowItems from "./components/ShowItems.vue";
import AddItems from "./components/AddItems.vue";
export default {
  name: "App",
  components: {
    Todo,
    ShowItems,
    AddItems
  },
  data() {
    return {
      itemList: [
        { id: 1, name: "Megha", marked: true },
        { id: 2, name: "Suyash", marked: false },
        { id: 3, name: "Yadav", marked: true }
      ]
    };
  },
  methods: {
    add(newItem) {
      this.itemList = [...this.itemList, newItem];
    }
  }
};
</script>

<style>
</style>
