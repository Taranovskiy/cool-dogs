<template>
  <button
    class="sort-toggle"
    :class="{ 'sort-toggle--on': isOn }"
    type="button"
    @click="sortToggle"
    :aria-label="text"
  >
    {{ text }}
    <span class="sort-toggle__control"></span>
  </button>
</template>

<script>
export default {
  name: "SortToggle",
  props: {
    text: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      isOn: false
    };
  },
  methods: {
    sortToggle() {
      this.isOn = !this.isOn;
      this.$emit("sort-on");
    }
  }
};
</script>
