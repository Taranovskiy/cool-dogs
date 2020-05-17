<template>
  <ul class="photos-list">
    <li
      v-for="(item, index) in 20"
      class="photos-list__item"
      :class="{ 'photos-list__item--big': index === 0 }"
      :key="index"
    >
      <photo-item :class="{ 'photo-item--big': index === 0 }" />
    </li>
  </ul>
</template>

<script>
import PhotoItem from "@/components/PhotoItem";

export default {
  name: "PhotosList",
  components: {
    PhotoItem
  },
  props: {},
  data() {
    return {};
  },
  methods: {}
};
</script>
