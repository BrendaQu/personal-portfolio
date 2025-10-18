<template>
  <div id="SkillsSection">
    <div class="section-title">
      Skills
      <div class="period-style">.</div>
    </div>
    <div class="skills-wrapper">
      <div class="skills-item" v-for="skill in skillsList">
        <SkillsPill :pillSkillName="skill" />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import SkillsPill from "./SkillsPill.vue";

const skillsList = [
  "JavaScript",
  "TypeScript",
  "Python",
  "SQL",
  "Java",
  "Vue.js",
  "React.js",
  "HTML",
  "CSS",
  "Sass",
  "Bootstrap",
  "D3.js",
  "AWS",
  "Jest",
  "Playwright",
  "Git",
  "Figma",
  "Docker",
  "Jira",
  "Visual Studio Code",
];
</script>
<style lang="css" scoped>
.skills-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  padding: 10px;
}
.skills-item {
  padding: 8px;
}

@media (max-width: 625px) {
  .skills-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    padding: 10px;
  }
}

@media (max-width: 500px) {
  .skills-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 10px;
  }
}
</style>
