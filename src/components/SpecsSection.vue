<template>
  <section class="cards-section">
    <SpecsCard v-for="(card, i) in cards" :key="i" :card="card" />
  </section>
</template>

<script setup>
import SpecsCard from "./SpecsCard.vue";

import { ref, computed } from "vue";

let cards = ref([
  {
    img: computed(() => {
      return new URL("../assets/traffic.png", import.meta.url).href;
    }),
    hd: "ATC",
    p: "31 million Vehicles Counted <br/> 65 thousand ATCs",
  },
  {
    img: computed(() => {
      return new URL("../assets/camera.png", import.meta.url).href;
    }),
    hd: "TMC",
    p: "29 thousand Cameras <br/>installed 29 <br/>thousand TMCs",
  },
  {
    img: computed(() => {
      return new URL("../assets/home.png", import.meta.url).href;
    }),
    hd: "Interview",
    p: "461k Household Interviews <br/>InterviewRoadside <br/>InterviewPublic <br/>TransportationParking <br/>InterviewPedestrian <br/>Survey",
  },
]);
</script>

<style lang="scss" scoped>
.cards-section {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  max-width: 1140px;
  margin: 0 auto;
  padding: 60px 0;
  @media (max-width: 768px) {
    flex-direction: column;
    align-items: center;
    gap: 16px;
  }
}
</style>