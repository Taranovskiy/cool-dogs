<template>
  <router-link
    :to="{ name: 'favorites' }"
    class="favorites-link"
    active-class="favorites-link--active"
  >
    Избранные пёсели
    <heart-icon class="favorites-link__icon" />
  </router-link>
</template>

<script>
import HeartIcon from "@/assets/icons/heart.svg";

export default {
  name: "FavoritesLink",
  components: {
    HeartIcon
  }
};
</script>
