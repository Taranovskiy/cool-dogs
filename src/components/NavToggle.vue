<template>
  <button
    class="nav-toggle"
    :class="{ 'nav-toggle--open': isTop }"
    type="button"
    @click="openNav"
    aria-hidden="true"
  >
    {{ text }}
    <arrow-icon class="nav-toggle__icon" />
  </button>
</template>

<script>
import ArrowIcon from "@/assets/icons/arrow-bottom.svg";

export default {
  name: "NavToggle",
  components: {
    ArrowIcon
  },
  props: {
    text: {
      type: String,
      default: ""
    },
    isOpen: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      isTop: this.isOpen
    };
  },
  methods: {
    openNav() {
      this.isTop = !this.isTop;
      this.$emit("open-nav");
    }
  }
};
</script>
