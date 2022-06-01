<template>
  <div id="app">
  <AppHeader />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  name: "App",
  components: {
    AppHeader,
  },
};
</script>

<style lang="scss">
*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.container{
  width: 1200px;
  margin: 0 auto;
}

ul {
  list-style-type: none;
}

.clearfix::after{
  content: "";
  display: table;
  clear: both;
}

.fl{
  float: left;
}

header{
  background-color: #0a1750;
  height: 680px;
  background-image: url("./assets/images/header.png");
  background-repeat: no-repeat;
  background-size: 40%;
  background-position: 80% 60%;
}

header .jumbotron h1 {
  width: 380px;
  margin-top: 100px;
  color: #fff;
  font-size: 45px;
}
header .jumbotron span {
  font-weight: normal;
  margin: 5px 0;
}
header .jumbotron p {
  margin-top: 30px;
  width: 400px;
  color: #03a7d3e6;
}

.services {
  text-align: center;
}
.services-list {
  display: flex;
  justify-content: space-between;
} 

button {
  background: linear-gradient(to right, #ff5db1 0%, #ef017c 100%);
  border-radius: 25px;
  width: 120px;
  height: 40px;
  border: none;
  color: #fff;
}

</style>
