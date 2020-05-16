<template>
  <header class="main-header">
    <div class="main-header__container">
      <div class="main-header__logo">
        <the-logo />
      </div>
      <div class="main-header__favorites">
        <favorites-link />
      </div>
    </div>
  </header>
</template>

<script>
import TheLogo from "@/components/TheLogo";
import FavoritesLink from "@/components/FavoritesLink";

export default {
  name: "TheHeader",
  components: {
    TheLogo,
    FavoritesLink
  }
};
</script>
