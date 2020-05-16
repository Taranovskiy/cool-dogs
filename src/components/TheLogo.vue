<template>
  <router-link
    :to="{ name: 'home' }"
    class="logo"
    active-class="logo--active"
    exact
  >
    <logo-icon />
  </router-link>
</template>

<script>
import LogoIcon from "@/assets/icons/logo.svg";

export default {
  name: "TheLogo",
  components: {
    LogoIcon
  }
};
</script>
