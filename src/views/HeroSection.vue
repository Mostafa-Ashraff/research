<template>
  <section class="hero">
    <NavBar />
    <div class="hero-content">
      <h4 class="hero-subtitle">Research</h4>
      <h1 class="hero-title">
        Beyond Numbers !<br />
        Intelligent Transport Analysis
      </h1>
      <p>
        We are a leading statistical research company with over 15 years of
        experience specializing in transport and traffic studies, data
        collection, and home surveys. With our integrated and diversified team,
        we strive to provide accurate and timely data, facilitated by our
        cutting-edge artificial intelligence technology and top-of-the-line
        traffic statistics cameras.
      </p>
    </div>
  </section>
</template>

<script setup>
import NavBar from "../components/navbar/NavBar.vue";
</script>

<style lang="scss" scoped>
.hero {
  background-image: url("../assets/hero-bg.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  min-height: 100vh;
  .hero-content {
    margin-top: 80px;
    margin-left: 88px;
    text-transform: uppercase;
    @media (max-width: 768px) {
      margin-left: 5px;
      margin-top: 40px;
    }
    .hero-subtitle {
      color: var(--accent-color);
      font-size: 18px;
      font-weight: 700;
      line-height: 24px;
      margin-bottom: 8px;
      @media (max-width: 768px) {
        font-size: 14px;
        line-height: 18px;
      }
    }
    .hero-title {
      color: var(--text-light);
      font-family: var(--header-font);
      font-size: 56px;
      font-weight: 600;
      line-height: 72px;
      margin-bottom: 40px;
      @media (max-width: 768px) {
        font-size: 32px;
        line-height: 46px;
        margin-bottom: 20px;
      }
    }
    p {
      max-width: 840px;
      text-transform: none;
      font-size: 20px;
      font-weight: 400;
      line-height: 30px;
      @media (max-width: 768px) {
        font-size: 16px;
        line-height: 24px;
      }
    }
  }
}
</style>