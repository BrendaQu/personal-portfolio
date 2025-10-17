<template>
  <div class="experience-wrapper">
    <div class="section-title">Experience.</div>
    <div v-for="job in experienceObjList">
      <ExperienceCard
        :cardCompany="job.companyName"
        :cardCompanyTitle="job.companyTitle"
        :cardCompanyDescription="job.companyDes"
        :cardCompanyYears="job.companyYears"
      />
    </div>
  </div>
</template>
<script lang="ts" setup>
import ExperienceCard from "../components/ExperienceCard.vue";
const experienceObjList = [
  {
    companyName: "Bloomberg Industry Group",
    companyTitle: "Software Engineer",
    companyDes:
      "Led front-end development and data visualizations at Bloomberg Government using Vue.js and D3.js, implemented unit testing with Jest, and tracked user interactions with analytics. Built reusable components and delivered polished, scalable features in a fast-paced, agile environment.",
    companyYears: "2022 - 2024",
  },
  {
    companyName: "Revature",
    companyTitle: "Software Engineer",
    companyDes:
      "Completed intensive full-stack training and contracted to Bloomberg Industry Group, working with Java, React.js, TypeScript, Spring Boot, MySQL, and Docker. Built interactive full-stack applications, led UI/UX design, and collaborated with a 20-person team to deliver polished, responsive projects praised by instructors and stakeholders.",
    companyYears: "2021 - 2023",
  },
  {
    companyName: "GSI Service Group",
    companyTitle: "Systems Specialist",
    companyDes:
      "Built and optimized systems at GSI Service Group, creating a Microsoft Access database that cut reporting time in half and improved user experience. Enhanced the company website, streamlined HR and recruiting systems, and drove higher engagement from employees and applicants.",
    companyYears: "2019 - 2021",
  },
];
</script>
<style lang="css">
.experience-wrapper {
  display: block;
  text-align: left;
}
</style>
