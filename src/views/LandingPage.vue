<template>
  <div>
    <HeroSection />
    <div class="container">
      <SpecsSection />
      <DetailsSection />
      <PartnerSection />
    </div>
    <FooterSection />
  </div>
</template>

<script setup>
import HeroSection from "./HeroSection.vue";
import SpecsSection from "../components/SpecsSection.vue";
import DetailsSection from "../components/DetailsSection.vue";
import PartnerSection from "../components/PartnerSection.vue";
import FooterSection from "../components/FooterSection.vue";
</script>
<style>
.container {
  @media (max-width: 768px) {
    padding: 0px 24px;
  }
}
</style>