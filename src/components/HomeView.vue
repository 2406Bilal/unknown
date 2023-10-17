<template>
    <div>
      <h1>home</h1>
      <p>my name is {{ name }} and my age is {{ age }} </p>
      <button @click="updateOne">click me to add </button>
  
    </div>
  </template>
  <script>
  export default {
    name: 'Home',
    setup() {
      let name = 'bilol'
      let age = 20
      return { name: name, age: age }
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
  
  nav {
    padding: 30px;
  }
  
  nav a {
    font-weight: bold;
    color: #2c3e50;
  }
  
  nav a.router-link-exact-active {
    color: #42b983;
  }
  </style>
  