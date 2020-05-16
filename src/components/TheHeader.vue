<template>
  <header class="main-header">
    <div class="main-header__container">
      <div class="main-header__logo">
        <the-logo />
      </div>
      <div class="main-header__favorites">Favorites</div>
    </div>
  </header>
</template>

<script>
import TheLogo from "@/components/TheLogo";

export default {
  name: "TheHeader",
  components: {
    TheLogo
  }
};
</script>
