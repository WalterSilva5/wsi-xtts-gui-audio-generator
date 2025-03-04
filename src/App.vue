<template>
  <div style="margin: 0; padding: 0"><page /></div>
</template>

<script>
import Page from "./components/Page.vue";
export default {
  components: {
    Page,
  },
};
</script>

<style lang="scss">
$primary-color: #007acc;
$secondary-color: #f0f8ff;
$text-color: #333;

body {
  background-color: $secondary-color;
  color: $text-color;
}

a {
  color: $primary-color;
  &:hover {
    color: darken($primary-color, 10%);
  }
}
</style>
