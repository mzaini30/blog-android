<script setup="" lang="ts">
import { onMounted } from "vue";
import tulisan from "../tulisan";
import { acak } from "kumpulan-tools";

const tulisanLainnya = acak(tulisan).slice(0, 5);

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
    <h2>Tulisan Lainnya</h2>
    <ul>
      <li v-for="x in tulisanLainnya">
        <router-link :to="`/tulisan/${x.slug}`">{{ x.judul }}</router-link>
      </li>
    </ul>
  </div>
</template>
