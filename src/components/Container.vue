<template>
  <div class="container">
    <slot></slot>
  </div>
</template>
<script setup>
defineProps({
  width: {
    type: Number,
    default: 1000,
  },
  mgBottom: {
    type: Number,
    default: 104,
  },
});
</script>
<style scoped>
.container {
  margin: 0 auto;
  max-width: v-bind(width + "px");
  width: 100%;
  padding: 0 30px;
  margin-bottom: v-bind(mgBottom + "px");
  /* background-color: wheat; */
}
</style>