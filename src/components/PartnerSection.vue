<template>
  <section class="partner-section">
    <h2>Our <span>Clients</span></h2>
    <Swiper
      :slidesPerView="isMobile ? 3 : 6"
      :pagination="{ dynamicBullets: true, dynamicMainBullets: 6 }"
    >
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
      <swiper-slide><img src="../assets/white-logo.png" alt="" /></swiper-slide>
    </Swiper>
  </section>
</template>

<script>
import { ref, watchEffect } from "vue";
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/pagination";
import { Pagination } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const isMobile = ref(window.innerWidth <= 768);

    return {
      modules: [Pagination],
      isMobile,
    };
  },
};
</script>

<style lang="scss" scoped>
.partner-section {
  padding: 80px 0;
  h2 {
    font-family: var(--header-font);
    font-size: 72px;
    font-weight: 700;
    line-height: 110px;
    text-align: center;
    margin-bottom: 64px;
    @media (max-width: 768px) {
      font-size: 42px;
      line-height: 52px;
    }
    span {
      color: var(--primary-color);
    }
  }
  .swiper {
    max-width: 1400px;
    margin: auto;
    img {
      max-width: 158px;
      @media (max-width: 768px) {
        max-width: 100px;
      }
    }
  }
}
</style>