<template>
  <div>
    <div v-for="items in itemLists" v-bind:key="items.id">
      <p>
        <input type="checkbox" v-on:change="checkMarked(item.id)" v-model="items.marked" />
        {{items.name}}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "ShowItems",
  props: ["itemLists"],
  methods: {
    checkMarked(event, id) {
      this.itemLists.forEach(element => {
        if (element.id == id) {
          element.marked = !element.marked;
        }
      });
      console.log(this.itemLists);
    }
  }
};
</script>