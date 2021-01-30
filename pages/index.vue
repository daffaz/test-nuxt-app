<template>
  <div>
    <Navbar />
    <div class="container">
      <Hero />
      <DisplayCardLarge v-for="data in bigCard" :key="data.id" :props="data" />
      <DisplayCardSmall v-for="data in smolCard" :key="data.id" :props="data" />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data";
export default {
  data() {
    return {
      bigCard: largeCardSections,
      smolCard: smallCardSections,
    };
  },
};
</script>

<style>
</style>
