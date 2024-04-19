<template>
   <nav class="navigation">
      <router-link to="/" class="nav-home">Home |</router-link>
      <router-link to="/productList" class="nav-task"> Product List</router-link> 
    </nav>
  <router-view/>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
    };
  },
  methods: {

  }
};
</script>

<style>
nav{
  text-align: center
}
#app {
  font-family: Arial;
  margin: 20px;
}
</style>
