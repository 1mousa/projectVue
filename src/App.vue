<template>

  <label for="search">Name:</label>
  <input type="text" name="search" id="search">
</template>

<script >
console.log("salam")
import FirstName from './components/FirstName.vue'
import LastName from './components/LastName.vue'
 import axios from 'axios'
export default {
  name: 'App',
mounted(){
axios({
  method: "get",
  url: "https://www.balldontlie.io/api/v1/players",
})
.then(function (response) {
  console.log(response);
});
}
}
  components: {FirstName , LastName}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
