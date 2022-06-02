<template>
  <header>
    <div class="container">
      <div class="navbar">
        <div class="navbar-left">
          <img class="logo" require:src="logo" alt="" />
        </div>
        <div class="navbar-right">
          <ul>
         <li
              v-for="(item, index) in navbarLinks"
              :key="index"
              :class="{ selected: item.active }"
            >
              {{ item.testo }}
            </li>
            <li> <button class="blue-button"> Sign In</button></li>
          </ul>
        </div>
      </div>
      <div class="jumbotron">
        <h1>
          Businnes Planning
          <span class="weight-normal">Digital Technology</span>
          Modern Solution!
        </h1>
        <p>
          When, while the lovely valley teems witch vapour around meand the
          meridian sun strikes the upper surface.
        </p>
        <button class="pink-button">Try It Now</button>
        <button class="blue-button">Explore More</button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
 data() {
    return {
      navbarLinks: [
        {
          testo: "Home",
          link: "#",
          active: true,
        },
        {
          testo: "About",
          link: "#",
          active: false,
        },
        {
          testo: "Services",
          link: "#",
          active: false,
        },
        {
          testo: "Blog",
          link: "#",
          active: false,
        },
        {
          testo: "Contact",
          link: "#",
          active: false,
        },
        {
          testo: "Portfolio",
          link: "#",
          active: false,
        },
      ],
    };
  },

};
</script>

<style lang="scss" scooped>
</style>