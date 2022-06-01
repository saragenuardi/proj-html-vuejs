<template>
  <div id="app">
    <AppHeader />
    <AppServices />
    <AppBusiness />
    <AppPortfolio />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppServices from "./components/AppServices.vue";
import AppBusiness from "./components/AppBusiness.vue";
import AppPortfolio from "./components/AppPortfolio.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppServices,
    AppBusiness,
    AppPortfolio,
  },
};
</script>

<style lang="scss">
//VARIABILI

//Colori
$blue-background: #0a1750;
$services-p: #808080;
$span: #f9696b;
//utilizzo gradient per la sfumatura dei bottoni
$gradient-pink-button: linear-gradient(to right, #b7256e 0%, #f8626b 100%);
$gradient-blue-button: linear-gradient(to right, #03a6d2 0%, #1f3e83 100%);
$blue-p: #047caa;

//Fonts
$font-body: "Open Sans", sans-serif;
$font-title: "Heebo", sans-serif;

//Bottons and mixin
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
@mixin flex-space-evenly {
  display: flex;
  justify-content: space-evenly;
}

//RESET
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

//COMMON
body {
  font-family: $font-body;
}
.container {
  width: 1200px;
  margin: 0 auto;
}

h1,
h2,
h3 {
  font-family: $font-title;
}

.weight-normal {
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

.pink-button {
  background: $gradient-pink-button;
  @include buttons-style();
}

.blue-button {
  background: $gradient-blue-button;
  @include buttons-style();
  margin-left: 20px;
}

//Header
header {
  background-color: $blue-background;
  height: 680px;
  background-image: url("./assets/images/header.png");
  background-repeat: no-repeat;
  background-size: 40%;
  background-position: 80% 60%;
  margin-bottom: 60px;

  .navbar {
    height: 90px;
    display: flex;
    align-items: center;
  }

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
      margin-bottom: 55px;
      width: 400px;
      color: $blue-p;
    }
  }
}

//Section SERVICES

.services {
  text-align: center;

  > span {
    color: $span;
  }

  h2 {
    margin: 15px 0;
  }

  p {
    color: $services-p;
  }

  &-list {
    @include flex-space-evenly();
    text-align: center;

    img {
      width: 125px;
      height: 100px;
      margin-top: 100px;
    }

    h3 {
      margin-top: 30px;
      margin-bottom: 20px;
    }

    p {
      color: $services-p;
      width: 200px;
    }
  }
  button {
    margin-top: 90px;
  }
}
//Section BUSINESS

.grow-your-business-section {
  background-color: #0a1750;
  height: 700px;
  color: #fff;
  margin-top: 70px;
  background-image: url("./assets/images/men-data.png");
  background-repeat: no-repeat;
  background-size: 27%;
  background-position: 20% 60%;
  margin-bottom: 60px;
  display: flex;
  align-items: center;

  .grow-your-business {
    margin-left: 650px;
  }

  h2 {
    width: 410px;
    margin-top: 30px;
    font-size: 45px;
  }

  p {
    width: 400px;
    margin-top: 30px;
    margin-bottom: 40px;
    color: $blue-p;
  }
}

//Section PORTFOLIO

.portfolio-section{

  &-content{
    margin-bottom: 30px;
    > span{
      color: $span;
    }
  }
  &-content-img{
    @include flex-space-between();

    img{
      width: 350px;
    }
  }
}
</style>
