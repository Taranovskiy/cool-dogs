<template>
  <div class="page__photos-list">
    <photos-list />
  </div>
</template>

<script>
import PhotosList from "@/components/PhotosList";

export default {
  name: "Home",
  components: {
    PhotosList
  }
};
</script>
