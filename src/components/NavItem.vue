<template>
  <router-link
    :to="path"
    class="nav-item"
    active-class="nav-item--active"
    exact
  >
    {{ name }}
  </router-link>
</template>

<script>
export default {
  name: "NavList",
  props: {
    name: {
      type: String,
      default: ""
    },
    isToHome: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    path() {
      return this.isToHome ? "/" : `/${this.name}`;
    }
  }
};
</script>
