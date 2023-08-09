<template>
  <nav class="navbar">
    <div class="navbar-left">
      <a href="/" class="navbar-logo">
        <img src="../../assets/white-logo.png" alt="Logo" />
      </a>
    </div>
    <div v-if="!isMobile" class="navbar-center">
      <a href="#about" class="navbar-link">About Us</a>
      <a href="#partners" class="navbar-link">Projects</a>
      <a href="#team" class="navbar-link">Our Team</a>
    </div>
    <div v-if="!isMobile" class="navbar-right">
      <ContactUs />
    </div>
    <div v-else class="navbar-mobile-menu" :class="{ 'is-open': isMenuOpen }">
      <div class="burger-menu" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <div class="navbar-mobile-links">
        <a href="#home" class="navbar-link">Home</a>
        <a href="#projects" class="navbar-link">Projects</a>
        <a href="#team" class="navbar-link">Our Team</a>
        <ContactUs />
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, watchEffect } from "vue";
import ContactUs from "./ContactUs.vue";
// import '@/assets/fonts.css'

const isMobile = ref(false);
const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

watchEffect(() => {
  if (window.innerWidth <= 768) {
    isMobile.value = true;
  } else {
    isMobile.value = false;
    isMenuOpen.value = false;
  }
  console.log(isMobile.value);
});
</script>

<style lang="scss" scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 20px 24px;
}

.burger-menu {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 3px;
  align-items: center;
  width: 40px;
  height: 40px;
  cursor: pointer;
  background-color: #fff;
  border-radius: 50%;

  span {
    width: 24px;
    height: 3px;
    border-radius: 30px;
    background-color: #595959;
    transition: all 0.3s ease-in-out;
  }
}

.is-open {
  background-color: #fff;
  width: 100%;
  height: 100vh;
  position: absolute;
  top: 0;
  left: 0;
  .burger-menu span:nth-child(1) {
    transform: translateY(6px) rotate(45deg);
  }
  .burger-menu span:nth-child(2) {
    opacity: 0;
  }
  .burger-menu span:nth-child(3) {
    transform: translateY(-6px) rotate(-45deg);
  }

  .navbar-mobile-links {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 20px;
    color: var(--secondary-color);
    a,
    a:visited {
      margin: 0 5%;
      text-decoration: none;
      color: var(--secondary-color);
    }
  }
}
.navbar-mobile-links {
  display: none;
}

@media (min-width: 768px) {
  .navbar {
    padding: 24px 88px;
    .navbar-center {
      width: 40%;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10%;

      a,
      a:visited {
        text-decoration: none;
        color: #fff;
        font-size: 20px;
        font-weight: 400;
        line-height: 30px;
      }
      a:hover {
        color: var(--accent-color);
      }
    }
  }
}
</style>