<template>
  
<footer>
    <div class="container">
      <div class="footer-content">
        <div class="footer-content-column-a">
          <img class="logo" :src="logo" alt="">
          <p>When, while lovely valley teems vapour aroundmeand meridian sun strikes the upper impenetrable</p>
        </div>
        <div class="footer-content-column-b">
          <h3>Quick Links</h3>
          <ul>
            <!-- <li v-for="element in footerQuickLinks"> <a href="">{{element}}</a> </li> -->
          </ul>
        </div>
        <div class="footer-content-column-c">
          <h3>Resources</h3>
          <ul>
            <!-- <li v-for="element in footerResources"> <a href="">{{element}}</a> </li> -->
          </ul>
        </div>
        <div class="footer-content-column-d">
          <h3>Contact Us</h3>
          <ul>
            <!-- <li v-for="element in footerContactUs"> 
              <p> <span>Address:</span> {{element.address}}</p>
              <p> <span>Phone:</span> {{element.phone}}</p>
              <p> <span>Email:</span> {{element.email}}</p>
            </li> -->
          </ul>
        </div>
      </div>
      
    </div>
    <hr>
    <div class="container">
      <div class="credits">
        <div class="credits-left">
          <p>© 2020 Phlox. All Rights Reserved.</p>
        </div>
        <div class="credits-right">
          <i class="fab fa-instagram"></i>
          <i class="fab fa-linkedin-in"></i>
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
        </div>
      </div>
    </div>
  </footer>
   
</template>

<script>
export default {
  name: "AppFooter",
  

};
</script>

 <style lang="scss">
$primary-background-color: #0a1750;
$footer-text-color: #aaa;
$color-4: #aaa;
$color-5: #69717b;

@mixin flex-space-between {
  display: flex;
  justify-content: space-between;
}

footer {
  background-color: $primary-background-color;
  height: 540px;
  margin-top: 205px;

  .footer-content {
    padding-top: 200px;
    @include flex-space-between();

    a {
      color: $color-5;
    }

    h3 {
      color: #fff;
      font-size: 16px;
      padding-bottom: 15px;
    }

    &-column-a {
      width: 280px;

      p {
        color: $color-4;
        margin-top: 35px;
        font-size: 13px;
      }
    }
  }
}

li {
  padding-bottom: 13px;

  &-column-c {
    padding-top: 15px;
    li {
      padding-bottom: 13px;
    }
  }
  &-column-d {
    padding-top: 15px;
    width: 300px;
    color: $color-5;

    span {
      color: #fff;
    }

    p {
      margin-bottom: 5px;
    }

    p:first-child {
      margin: 5px 0 20px 0;
    }
  }

  hr {
    margin-top: 40px;
    border: none;
    height: 0.5px;
    background-color: $color-5;
    margin-bottom: 20px;
  }
  .credits {
    @include flex-space-between();

    &-left {
      color: $color-5;
    }
    &-right {
      i {
        padding-left: 30px;
        font-size: 14px;
        color: #fff;
      }
    }
  }
}
</style>