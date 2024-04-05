<template>
  <nav class="navbar">
    <a class="navbar__logo" href="/">Shop Verse</a>
    <div class="navbar__menu">
      <a class="navbar__menu--link" href="/">About</a>
      <a class="navbar__menu--link" href="/">Shop</a>
      <a class="navbar__menu--link" href="/">Categories</a>
      <a class="navbar__menu--link" href="/">Help</a>
    </div>
    <div class="navbar__icons">
      <div class="navbar__icons--icon"><i class="fa fa-heart-o fa-lg"></i></div>
      <div class="navbar__icons--icon"><i class="fa fa-shopping-basket fa-lg" aria-hidden="true"></i></div>
    </div>
  </nav>
</template>

<script>
import Heart from "@/assets/icons-svg/Heart.vue";
import CartIcon from "@/assets/icons-svg/CartIcon.vue";

export default {
  name: "NavBar",
  components: {CartIcon, Heart}
}
</script>

<style lang="scss" scoped>
@import "../assets/_colors.scss";

.navbar {
  display: flex;
  background-color: $light;
  align-items: center;
  height: 80px;
  justify-content: space-between;
  padding: 0.5rem calc((100vw - 1200px) / 2);
  z-index: 10;
  position: relative;

  &__logo {
    text-decoration: none;
    color: $dark;
    padding: 24px;
  }

  &__menu {
    display: flex;

    &--link {
      margin: 5px;
      text-decoration: none;
      color: $dark;
    }
  }

  &__icons {
    display: flex;
    padding: 24px;
    &--icon {
      margin: 5px;
    }
  }
}
</style>

