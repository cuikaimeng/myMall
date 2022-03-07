<template>
  <div class="container">
    <Header></Header>
    <div class="container">
      <div class="aside"></div>
      <div class="main"></div>
    </div>
    <div class="footer"></div>
  </div>
</template>
<script>
  import Header from '../components/Header'
  export default {
    name: "Home",
    components: {
      Header
    },
    data() {
      return {
        msg: "Go",
      };
    }
  };
</script>
<style scoped>
  .container {
    margin: 0;
    padding: 0;
  }
</style>
