<template>
  <div id="app">
    <h1>Shopping List</h1>
  </div>
  <ul>
    <li v-for="item of items" :key="item.id">
      {{ item.title }}
    </li>
  </ul>
</template>

<script>
import axios from "axios";

export default {
  name: "MainPage",
  data() {
    return {
      items: [],
    };
  },
  async created() {
    try {
      const res = await axios.get(`http://localhost:3000/MenuItems`);
      this.items = res.data;
    } catch (error) {
      console.log(error);
    }
  },
};
</script>
<style>

</style>