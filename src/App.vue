<template>
  <div id="app">
   
    <BiscuitPage />
  </div>
</template>

<script>
import BiscuitPage from './components/BiscuitPage.vue';

export default {
  name: 'App',
  components: {
    BiscuitPage
  }
};
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  margin: 20px;
}
.h1{
  text-align: center;
}
</style>
