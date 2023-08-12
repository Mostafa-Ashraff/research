<template>
  <section class="video-section">
    <!-- <iframe
      width="80%"
      height="500"
      src="https://www.youtube.com/embed/JSmgceKvy5Y?controls=0"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    ></iframe> -->
    <video id="presentation-vid" autoplay>
      <source src="../assets/video-src.mp4" />
    </video>
  </section>
</template>

<script setup>
import { onMounted, watchEffect } from "vue";

onMounted(() => {
  //   let videoElement = document.querySelector(".video-section");
  // document.querySelector('.hero').offsetHeight

  //   let observer = new IntersectionObserver(function (entries) {
  //     entries.forEach(function (entry) {
  //       if (entry.intersectionRatio > 0.7) {
  //         videoElement.play();
  //       } else {
  //         console.log("The div is not in view!");
  //       }
  //     });
  //   });
  //   observer.observe(videoElement);
  let heroSectionHeight = document.querySelector(".hero").offsetHeight;
  const videoElement = document.querySelector("#presentation-vid");

  // watchEffect(() => {
  //   window.addEventListener("scroll", () => {
  //     let scrollY = window.scrollY;
  //     if (scrollY > heroSectionHeight / 2) {
  //       videoElement.play();
  //       console.log("play");
  //     }
  //   });
  // });
});
</script>

<style lang="scss" scoped>
.video-section {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 60px 0px;
  video {
    width: 100%;
  }
}
</style>