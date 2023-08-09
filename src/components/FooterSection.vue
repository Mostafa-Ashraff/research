<template>
  <div>
    <footer class="d-flex align-items-center">
      <div class="icons">
        <div class="logo"><img src="../assets/white-logo.png" alt="" /></div>
      </div>
      <div class="explore">
        <h2>Explore</h2>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="">About Us</a></li>
          <li><a href="">Contact</a></li>
        </ul>
      </div>
      <div class="contact">
        <h2>Contact</h2>
        <ul>
          <li><a href="">Email</a></li>
          <li><a href="">Phone</a></li>
          <li><a href="">Address</a></li>
        </ul>
      </div>
      <div class="get-in-touch">
        <p>Privacy Policy</p>
        <p>Terms & Condition</p>
      </div>
    </footer>
    <div class="copyright d-flex flex-column">
      <hr />
      <div class="copyright-info">
        <p>
          Copyright © 2023 Research-sa.<br />
          All rights reserved.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
footer {
  padding: 40px 20px;
  gap: 24px;
  flex-direction: column;
  color: #fff;
  background-color: var(--secondary-color);
  .logo {
    @media (max-width: 768px) {
      width: 112px;
    }
  }
  h2 {
    margin-bottom: 16px;
    font-weight: 600;
  }
  ul {
    display: flex;
    flex-direction: column;
    gap: 16px;
    list-style: none;
    padding-left: 0px;
    margin-bottom: 0px;
    li a,
    li a:hover,
    li a:visited {
      color: #fff;
      text-decoration: none;
    }
  }
  @media (min-width: 768px) {
    flex-direction: row;
    justify-content: space-between;
  }
}
.copyright {
  background-color: var(--secondary-color);
  opacity: 0.85;
  text-align: left;
  flex-direction: column;
  .copyright-info {
    @media (min-width: 768px) {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
    }
  }
  hr {
    margin-bottom: 16px;
    color: #fff;
  }
  p {
    font-size: 12px;
    line-height: 18px;
    margin-bottom: 8px;
    max-width: 700px;
  }
}
</style>