<template>
  <section class="partner-section" id="clients">
    <h2>Our <span>Clients</span></h2>
    <Swiper
      :slidesPerView="isMobile ? 3 : 6"
      :pagination="{ dynamicBullets: true, dynamicMainBullets: 6 }"
      spaceBetween="10"
    >
      <swiper-slide v-for="(client, i) in clients" :key="i"
        ><img :src="client.img" alt=""
      /></swiper-slide>
    </Swiper>
  </section>
</template>

<script>
import { ref, computed } from "vue";
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
    const clients = ref([
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/amanah-gedda.png",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/CDM-Smith.jpg", import.meta.url)
            .href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/Dornier.jpg", import.meta.url)
            .href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/esri.jpeg", import.meta.url)
            .href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/FAST.jpg", import.meta.url).href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/fawaz-alhokair.jpeg",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/inneco.jpeg", import.meta.url)
            .href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/metro-count.png",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/panda-logo.png", import.meta.url)
            .href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/railways-org.jpeg",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/riyadh-train.png",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/transsportation-minstiry.jpeg",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/wilbur-smith.jpeg",
            import.meta.url
          ).href;
        }),
      },
      {
        img: computed(() => {
          return new URL("../../public/clients/ZFP.png", import.meta.url).href;
        }),
      },
      {
        img: computed(() => {
          return new URL(
            "../../public/clients/الهيئة العليا لتطوير الرياض.jpg",
            import.meta.url
          ).href;
        }),
      },
    ]);
    return {
      modules: [Pagination],
      isMobile,
      clients,
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
      width: 80px !important;
      object-fit: contain;
      height: 50px !important;
      @media (min-width: 768px) {
        width: 100px !important;
        height: 65px !important;
      }
    }
  }
}
</style>