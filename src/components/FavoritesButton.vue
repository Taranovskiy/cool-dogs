<template>
  <button type="button" class="favorites-button" @click="active = !active">
    <heart-icon-fill v-if="active" class="favorites-button__icon" />
    <heart-icon v-else class="favorites-button__icon" />
  </button>
</template>

<script>
import HeartIcon from "@/assets/icons/heart.svg";
import HeartIconFill from "@/assets/icons/heart-fill.svg";

export default {
  name: "FavoritesButton",
  components: {
    HeartIcon,
    HeartIconFill
  },
  data() {
    return {
      active: false
    };
  }
};
</script>
