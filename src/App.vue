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
//VARIABILI

//Colori
$blue-background: #0a1750;

//Fonts

$font-body: 'Open Sans', sans-serif;
$font-title: 'Heebo', sans-serif; 
//RESET
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}


@mixin buttons-style {
  border-radius: 25px;
  width: 140px;
  height: 40px;
  border: none;
  color: #fff;
}
@mixin flex-space-between {
  display: flex;
  justify-content: space-between;
}

//COMMON
body {
  font-family: $font-body;
}
.container {
  width: 1200px;
  margin: 0 auto;
}

h1, h2, h3{
  font-family: $font-title;
}

.weight-normal{
  font-weight: normal;
}

ul {
  list-style-type: none;
}

.clearfix::after {
  content: "";
  display: table;
  clear: both;
}

.fl {
  float: left;
}

button {
  //Utilizzo gradient per la sfumatura
  background: linear-gradient(to right, #ff5db1 0%, #ef017c 100%);
  border-radius: 25px;
  width: 120px;
  height: 40px;
  border: none;
  color: #fff;
}

//Header
header {
  background-color: $blue-background;
  height: 680px;
  background-image: url("./assets/images/header.png");
  background-repeat: no-repeat;
  background-size: 40%;
  background-position: 80% 60%;

  .jumbotron {
    h1 {
      width: 380px;
      margin-top: 100px;
      color: #fff;
      font-size: 45px;
    }

    span {
      font-weight: normal;
      margin: 5px 0;
    }

    p {
      margin-top: 30px;
      width: 400px;
      color: #03a7d3e6;
    }
  }
}

.services {
  text-align: center;

  &-list {
    display: flex;
    justify-content: space-between;
  }
}
</style>
