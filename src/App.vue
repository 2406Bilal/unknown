<template>
  <div class="home">
    <h1>home</h1>
    <input type="text" v-model="search">
    <p> search term - {{ search}}</p>
    <p v-for="name in matchingNames" :key="name"> {{ name }}</p>
  </div>
</template>

<script>
import { computed, ref } from 'vue';
export default {
  name: 'Home',
  setup() {
    const search = ref('')
    const names = ref([' bilol', ' hasan', ' huseyn', 'awur', ' botasli'])

    const matchingNames = computed(() => {
      return names.value.filter((name) => name.includes(search.value))
    })


    return { names, search , matchingNames}
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
