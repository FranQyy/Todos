<template>
  <header class="header">
      <h2>Todo list</h2>
      <div id="nav">
        <router-link to="/">Home</router-link> | 
        <router-link to="/about">About</router-link>
      </div>
  </header>
</template>

<script>
export default {
  name: 'Header',

}
</script>

<style>
  .header{
    background: black;
    color: white;
    padding: 15px;
    text-align: center;
  }

  .header a{
    color: white;
    text-decoration: none;
  }
</style>