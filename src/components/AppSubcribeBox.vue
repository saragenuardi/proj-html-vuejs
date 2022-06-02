<template>
  <div class="subscribe-box">
    <div class="subscribe-box-left">
      <h2>We Offer Awesome Services</h2>
      <p>
        When, while the lovely valley teems with vapour around meand the
        meridian sun strikes the upper surface.
      </p>
    </div>
    <div class="subscribe-box-right">
      <input type="text" placeholder="Enter Your Email Address" />
      <button class="blue-button">Subscribe</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppSubcribeBox.vue",
};
</script>

<style lang="scss">
.subscribe-box {
  position: absolute;
  width: 100%;
  color: #fff;
  height: 220px;
  text-align: left;
  padding: 0 35px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: linear-gradient(to right, #b7256e 0%, #f8626b 100%);
  border-radius: 26px;
  //bottom

  &-left {
    h2 {
      font-size: 36px;
      margin-bottom: 2px;
    }
    p {
      font-size: 12px;
    }
  }
  &-right {
    display: flex;
    flex-direction: row;
    border-radius: 23px;
    background-color: #fff;
    width: 430px;

    input {
      height: 50px;
      width: 320px;
      border-radius: 29px;
      padding-left: 35px;
      border: none;
    }
    button {
      width: 110px;
      margin: 5px 7px 5px 0;
    }
  }
}
</style>>
