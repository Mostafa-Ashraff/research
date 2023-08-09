<template>
  <div class="spec-card">
    <img :src="card.img" alt="" />
    <div class="card-txt">
      <h4>{{ card.hd }}</h4>
      <p v-html="card.p"></p>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  card: {
    type: Object,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.spec-card {
  align-items: center;
  display: flex;
  flex-direction: column;
  gap: 16px;
  text-align: center;
  background-color: var(--secondary-color);
  color: var(--text-light);
  padding: 20px;
  border-radius: 10px;
  width: 350px;

  img {
    width: 54px;
  }
  h4 {
    font-family: var(--secondary-font);
    font-size: 18px;
    font-weight: 700;
    line-height: 32px;
  }
  p {
    font-size: 16px;
    font-weight: 400;
    line-height: 24px;
  }
}
</style>