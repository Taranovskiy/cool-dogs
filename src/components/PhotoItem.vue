<template>
  <div class="photo-item">
    <img
      class="photo-item__img"
      src="https://images.dog.ceo/breeds/greyhound-italian/n02091032_561.jpg"
      alt=""
    />
    <span class="photo-item__caption">Порода</span>
    <span class="photo-item__favorites-button">
      <favorites-button />
    </span>
  </div>
</template>

<script>
import FavoritesButton from "@/components/FavoritesButton";

export default {
  name: "PhotoItem",
  components: {
    FavoritesButton
  },
  props: {},
  data() {
    return {};
  },
  methods: {}
};
</script>
