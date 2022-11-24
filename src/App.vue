<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { defineAsyncComponent } from "vue"

const FileDrop = defineAsyncComponent(() =>import("./components/FileDrop.vue"))

function startUpload(files : File[]) : void {
  files.map(file => console.log("uploading"), file)
}
</script>

<template>


  <main>
    <div class="grid place-items-center mx-auto h-96">
      <FileDrop class="w-72 h-72" @upload="starUpload"/>
    </div>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
