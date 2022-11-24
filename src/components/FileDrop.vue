<script setup lang="ts">

</script>

<template>
  <label v-bind="$attrs" class="label ">
    <input multiple type="file" class="input">
    <span class="message">drop your file here</span>
  </label>

</template>

<style scoped>
.label{
  @apply relative transition-all ease-in-out duration-300 border border-gray-500;
}
.input {
  @apply absolute top-0 left-0 w-full h-full hidden;
}
.message {
  @apply absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2;
}
</style>