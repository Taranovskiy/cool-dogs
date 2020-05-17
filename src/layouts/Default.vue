<template>
  <div class="page">
    <div class="page__header">
      <the-header />
    </div>
    <main class="page__main">
      <div class="page__nav">
        <the-nav />
      </div>
    </main>
  </div>
</template>

<script>
import TheHeader from "@/components/TheHeader";
import TheNav from "@/components/TheNav";

export default {
  name: "Default",
  components: {
    TheHeader,
    TheNav
  }
};
</script>
