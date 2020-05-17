<template>
  <button
    v-if="currentPageName.length"
    class="nav-item nav-item--current"
    type="button"
    @click="close"
  >
    <span class="nav-item__caption">
      {{ currentPageName }}
    </span>
    <close-icon class="nav-item__close-icon"></close-icon>
  </button>
</template>

<script>
import CloseIcon from "@/assets/icons/close.svg";

export default {
  components: {
    CloseIcon
  },
  name: "NavList",
  data() {
    return {
      isDisplay: true
    };
  },
  computed: {
    currentPageName() {
      const pathAsArray = this.$route.path.split("/");
      return pathAsArray.pop();
    }
  },
  methods: {
    close() {
      this.$router.push({ name: "home" });
      this.isDisplay = false;
    }
  }
};
</script>
