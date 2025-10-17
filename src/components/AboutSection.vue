<template>
  <div class="about-me">
    <div class="about-me-text">
      <div>Hi, I'm Brenda Quach.</div>
      <div>Software Engineer.</div>
      <div class="about-summary">
        Frontend-focused engineer. I build intuitive interfaces and data
        visualizations that make complexity simple. I love crafting experiences
        that feel effortless to use.
      </div>
    </div>
    <div class="about-me-img">
      <img src="@/assets/profile-pic.png" />
    </div>
  </div>
</template>
<script lang="ts"></script>
<style lang="css">
.about-me {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 500px;
  justify-content: center;
  align-items: center;
  font-size: 30px;
}
.about-summary {
  width: 400px;
  font-size: 18px;
}
</style>
