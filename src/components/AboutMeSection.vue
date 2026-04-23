<template>
  <div id="AboutMeSection" class="about-me-wrapper">
    <div class="section-title">
      About Me
      <div class="period-style">.</div>
    </div>
    <div class="about-me-content">
      <div class="about-me-summary">
        <p>
          I'm a frontend-focused Software Engineer with 3+ years of experience
          building interactive, data-driven web applications. My path into
          software wasn't traditional, I started as an Environmental Engineering
          student at the
          <a
            class="about-me-link"
            href="https://www.colorado.edu/"
            target="_blank"
          >
            University of Colorado Boulder</a
          >, and in my junior year picked up a Computer Science minor out of
          curiosity. I quickly fell in love with it and knew I wanted to pursue
          software development. I went on to complete an intensive full-stack
          bootcamp with
          <a class="about-me-link" href="https://revature.com/" target="_blank">
            Revature </a
          >, which led to a contract role at
          <a
            class="about-me-link"
            href="https://www.bloombergindustry.com/"
            target="_blank"
          >
            Bloomberg Industry Group</a
          >
          where I was brought on full-time after demonstrating consistent impact
          on the team.
          <br />
          <br />
          At Bloomberg, I primarily worked on their
          <a
            class="about-me-link"
            href="https://about.bgov.com/"
            target="_blank"
          >
            Bloomberg Government</a
          >
          product, where I spent over three years crafting data visualizations
          and scalable UI features. A couple notable features I built include an
          interactive Sankey chart for the
          <a
            class="about-me-link"
            href="https://about.bgov.com/products/federal-budget-and-spending/"
            target="_blank"
            >Federal Budget and Spending Insight
          </a>
          product and a bill density heat map for the
          <a
            class="about-me-link"
            href="https://about.bgov.com/products/public-affairs-intelligence/federal-and-state-tracking/"
            target="_blank"
            >Federal and State Tracking</a
          >
          product.
          <br />
          <br />

          I specialize in Vue.js, D3.js, TypeScript, and Javascript, with a
          passion for turning complex data into interfaces that fell effortless
          to use. Outside of frontend work, I've been expanding into cloud
          architecture and infrastructure, earning three AWS certifications
          along the way.
        </p>
      </div>
      <div class="about-img">
        <img class="profile-img" src="@/assets/pic-sticker.png" width="250px" />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup></script>
<style lang="css">
.about-me-wrapper {
  width: 100%;
  max-width: 1280px;
  height: auto;
  padding-top: 20px;
}

.about-me-content {
  display: flex;
}

.about-me-summary {
  text-align: left;
  min-width: 360px;
  padding: 10px;
  padding-top: 20px;
  margin-left: 40px;
  margin-right: 20px;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 18px;
}

.about-me-link {
  text-decoration: none !important;
  color: #55a855 !important;
  position: relative;
  display: inline-block;
}

.about-me-link::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background-color: #55a855;
  transition: width 0.3s ease;
}

.about-me-link:hover::after {
  width: 100%;
}

.about-img {
  margin-right: 50px;
  padding: 50px;
}

.profile-img {
  border: 2px solid #5faf5f;
  border-radius: 50%;
  box-shadow: 10px 10px 5px #c5c5c5;
}

@media (max-width: 775px) {
  .about-me-summary {
    font-size: 16px;
  }
  .about-me-content {
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
