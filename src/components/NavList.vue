<template>
  <ul class="nav-list">
    <li v-if="textAll.length" class="nav-list__item nav-list__item--all">
      <nav-item :name="textAll" :is-to-home="true" />
    </li>
    <li
      v-for="(item, index) in list"
      class="nav-list__item"
      :class="{ 'nav-list__item--last': isLast(item, list[index + 1]) }"
      :key="`nav-item-${index}`"
    >
      <span
        v-if="isFirst(item, list[index - 1], index)"
        class="nav-list__item-letter"
      >
        {{ item[0] }}
      </span>
      <nav-item :name="item" />
    </li>
  </ul>
</template>

<script>
import NavItem from "@/components/NavItem";

export default {
  name: "NavList",
  components: {
    NavItem
  },
  props: {
    textAll: {
      type: String,
      default: ""
    },
    list: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      activeItem: "all"
    };
  },
  methods: {
    isFirst(current, prev, index) {
      if (index === 0) {
        return true;
      }
      if (prev && current) {
        return prev[0] !== current[0];
      }
      return false;
    },
    isLast(current, next) {
      if (current && next) {
        return current[0] !== next[0];
      }
      return false;
    }
  }
};
</script>
