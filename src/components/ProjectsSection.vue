<template>
  <div id="ProjectsSection">
    <div class="section-title">
      Projects
      <div class="period-style">.</div>
    </div>
    <div class="project-section-wrapper fade-in">
      <div v-for="project in projectList">
        <ProjectsCard
          :projectTitle="project.projectTitle"
          :projectLink="project.projectLink"
          :projectDescription="project.projectDescription"
          :projectSkills="project.projectSkills"
          :projectImg="project.projectImage"
          :projectGithub="project.projectGithub"
        />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import ProjectsCard from "./ProjectsCard.vue";

const projectList = [
  {
    projectTitle: "Activity Dashboard App",
    projectDescription:
      "Interactive dashboard for visualizing and exploring exercise activity data.",
    projectLink: "https://brendaqu.github.io/activity-dashboard/",
    projectGithub: "https://github.com/BrendaQu/activity-dashboard/",
    projectImage: "activity-dashboard.png",
    projectSkills: [
      "TypeScript",
      "React",
      "HTML",
      "CSS",
      "Recharts",
      "Material UI",
    ],
  },
  {
    projectTitle: "Simple Weather App",
    projectDescription:
      "Simple weather app displaying forecast for Next 5 days and hours.",
    projectLink: "",
    projectGithub: "https://github.com/BrendaQu/simple-weather-app",
    projectImage: "simple-weather-app.png",
    projectSkills: ["TypeScript", "Vue", "HTML", "CSS"],
  },
  {
    projectTitle: "Finance Tracker App",
    projectDescription:
      "Allows users to enter expenses and see monthly totals on their expenditures.",
    projectLink: "",
    projectGithub: "https://github.com/BrendaQu/project2-finance-tracker",
    projectImage: "finance-tracker-app.png",
    projectSkills: [
      "JavaScript",
      "Java",
      "HTML",
      "CSS",
      "Bootstap",
      "MySQL",
      "Spring",
    ],
  },
  {
    projectTitle: "Social Media App",
    projectDescription:
      "Social media app includes login, post, and profile pages.",
    projectLink: "",
    projectGithub: "https://github.com/Revature-MiniMint/front_end/",
    projectImage: "social-media-app.png",
    projectSkills: [
      "JavaScript",
      "React",
      "HTML",
      "CSS",
      "Bootstrap",
      "Java",
      "Spring",
    ],
  },
];
</script>
<style lang="css">
.project-section-wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 20px 0px;
}
</style>
