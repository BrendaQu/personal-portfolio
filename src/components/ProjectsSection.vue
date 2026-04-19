<template>
  <div id="ProjectsSection">
    <div class="section-title">
      Projects
      <div class="period-style">.</div>
    </div>
    <div class="project-section-wrapper">
      <div v-for="project in projectList">
        <ProjectsCard
          :projectTitle="project.projectTitle"
          :projectLink="project.projectLink"
          :projectDescription="project.projectDescription"
          :projectSkills="project.projectSkills"
        />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import ProjectsCard from "./ProjectsCard.vue";

const projectList = [
  {
    projectTitle: "Simple Weather App",
    projectDescription:
      "Simple weather app displaying forecast for Next 5 days and hours.",
    projectLink: "https://github.com/BrendaQu/simple-weather-app",
    projectSkills: ["TypeScript", "Vue", "HTML", "CSS"],
  },
  {
    projectTitle: "Finance Tracker App",
    projectDescription:
      "Allows users to enter expenses and see monthly totals on their expenditures.",
    projectLink: "https://github.com/BrendaQu/project2-finance-tracker",
    projectSkills: ["JavaScript", "Java", "HTML", "CSS"],
  },
  {
    projectTitle: "Social Media App",
    projectDescription:
      "Class wide project for social media app. Includes login, post, and profile pages.",
    projectLink: "https://github.com/Revature-MiniMint/front_end/",
    projectSkills: ["JavaScript", "React", "HTML", "CSS"],
  },
];
</script>
<style lang="css">
.project-section-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  margin-right: 20px;
  padding-right: 20px;
}
</style>
