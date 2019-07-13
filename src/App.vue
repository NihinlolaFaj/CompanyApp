<template>
  <div id="app">
    <div class="header">Company App</div>
    <Company />
    <div class="footer">Built by Nihinlolamiwa</div>
  </div>
</template>

<script>
import Company from "./components/Company.vue";

export default {
  name: "app",
  components: {
    Company
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.header {
  -webkit-margin-top-collapse: discard;
  margin-bottom: 3%;
  padding: 10px;
  height: 0%;
  text-align: center;
  background: #58585b;
  color: white;
  font-size: 30px;
  right: 0;
  top: 0;
}
.footer {
  margin-top: 50px;
  height: 40px;
  text-align: center;
  background: #58585b;
  color: white;
  font-size: 20px;
  padding-top: 1%;

  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  color: white;
  text-align: center;
}
</style>
