<script setup="" lang="ts">
import { onMounted } from "vue";
onMounted(() => {
  const adaH1 = document.querySelector("h1");
  if (adaH1) {
    document.title = adaH1.innerText;
  }
});
</script>

<template>
  <div class="tulisan prose mx-auto p-3">
    <router-view></router-view>
  </div>
</template>
