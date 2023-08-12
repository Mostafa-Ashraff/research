<template>
  <section class="details-section" id="about">
    <div
      class="detail d-flex justify-content-between align-items-center"
      v-for="(detail, i) in details"
      :key="i"
    >
      <div class="detail-txt">
        <h3>{{ detail.hd }}</h3>
        <p v-html="detail.p"></p>
      </div>
      <img :src="detail.img" alt="" />
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from "vue";

let details = ref([
  {
    img: computed(() => {
      return new URL("../assets/projects.png", import.meta.url).href;
    }),
    hd: "Prior Projects",
    p: "We have an impressive portfolio of significant projects that includes traffic surveys for the Riyadh Metro, economic and traffic studies for the three-stage Haramain sector project, and Master Plans for Jeddah, Makkah, and Riyadh. We are proud to be recognized and approved by Aramco.",
  },
  {
    img: computed(() => {
      return new URL("../assets/tech.png", import.meta.url).href;
    }),
    hd: "Equipment and Technology",
    p: "Our company provides a diverse range of statistical equipment, digital programs, and specialized software for data analysis and traffic surveys. With a highly qualified and experienced team available globally, we deliver accurate and efficient services. Our commitment to staying ahead in technology ensures reliable and insightful analysis for our clients.",
  },
  {
    img: computed(() => {
      return new URL("../assets/service.png", import.meta.url).href;
    }),
    hd: "Service Expectations",
    p: "Clients can expect professional and efficient services, encompassing comprehensive transport and traffic studies, meticulous data collection, and in-depth home surveys. Our expansive geographical reach, coupled with the expertise of our team and our reliance on advanced technology, assures the delivery of quality-driven, precise, and timely results.",
  },
]);
</script>

<style lang="scss" scoped>
.details-section {
  display: flex;
  flex-direction: column;
  max-width: 1140px;
  margin: 0 auto;
  padding: 40px 0;
  gap: 80px;

  .detail {
    @media (max-width: 768px) {
      flex-direction: column !important;
      gap: 24px;
    }
    .detail-txt {
      max-width: 490px;
      h3 {
        font-family: var(--header-font);
        font-size: 40px;
        font-weight: 600;
        line-height: 52px;
        text-align: left;
        margin-bottom: 40px;
      }
      p {
        font-size: 16px;
        font-weight: 400;
        line-height: 24px;

        text-align: left;
      }
    }
  }

  .detail:nth-child(even) {
    flex-direction: row-reverse;
  }
}
</style>