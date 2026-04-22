<template>
  <div id="ExperienceSection" class="experience-wrapper">
    <div class="section-title">
      Experience
      <div class="period-style">.</div>
    </div>

    <div class="experience-nav">
      <div class="exp-nav-side-panel">
        <button
          v-for="job in experienceObjList"
          :id="job.companyId + '-tab'"
          :class="['exp-nav-side-item', { active: job.companyVisible }]"
          @click="handleClick(job.companyId)"
        >
          {{ job.companyName }}
        </button>
      </div>
      <div class="exp-tab-content">
        <div v-for="job in experienceObjList" :id="job.companyId">
          <ExperienceCard
            :cardCompany="job.companyName"
            :cardCompanyTitle="job.companyTitle"
            :cardCompanyDescription="job.companyDes"
            :cardCompanyYears="job.companyYears"
            :cardCompanyLink="job.companyLink"
            :cardVisible="job.companyVisible"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import ExperienceCard from "../components/ExperienceCard.vue";
import { ref } from "vue";

const experienceObjList = ref([
  {
    companyId: "BIG",
    companyName: "Bloomberg Industry Group",
    companyTitle: "Software Engineer",
    companyDes: [
      "Spearheaded front-end development for a data visualization project; created an interactive flow diagram, responsive table, and advanced filtering functionalities, becoming the first of its kind in the government affairs industry.",
      "Led the development and release of an interactive US bill density map feature that was showcased at the National Conference of State Legislatures and drove significant sales impact for Bloomberg Government.",
      "Advocated unit testing practices with Jest, leading to improved code quality and a 70% increase in test coverage.",
      "Initiated the integration of D3.js library into the organization by creating a reactive chart feature, laying the foundation for extensive future data visualization projects. ",
      "Developed 9 greenfield frontend projects for Bloomberg Government using single-spa architecture with Vue.js, JavaScript, D3.js, HTML, CSS, and GraphQL, enhancing user experience for thousands of users.",
      "Implemented analytics tagging with Amplitude to capture user activity on new and legacy pages, successfully tracking and analyzing thousands of user interactions, providing valuable insights for data-driven decision making.",
      "Built CloudFormation templates to create cross-account S3 buckets with replication configuration and implement a Lambda trigger to copy incoming files to a central destination bucket.",
      "Onboarded new team members and updated technical documentation on VuePress site and Confluence, reducing onboarding time from one week to one day.",
      "Collaborated with product manager, UX designers, and external teams to translate project objectives and wireframes into polished user interfaces, while contributing effectively to an agile work environment.",
    ],
    companyYears: "Feb 2022 - Nov 2024",
    companyLink: "https://www.bloombergindustry.com/",
    companyVisible: true,
  },
  {
    companyId: "Rev",
    companyName: "Revature",
    companyTitle: "Software Engineer",
    companyDes: [
      "Contracted out to Bloomberg Industry Group after twelve weeks of intensive training on full stack web application development, specializing in Java, React.js, MySQL, JavaScript, TypeScript, HTML, CSS, Spring Boot, Docker, and JUnit. ",
      "Built three interactive full stack applications using object-oriented programming principles, collaborating with a team of 20 peers. Received positive feedback from instructors for code quality, responsive design, and demonstration. ",
      "Served as UI/UX Developer and Designer for a class wide project, delivering wireframes and a style guide to ensure design consistency across multiple teams, optimizing development efficiency and coherence. ",
      "Delegated tasks to teammates, ensuring 100% coverage of project objectives, and organized presentations and demos to stakeholders, resulting in positive feedback for project design and effectiveness.",
    ],
    companyYears: "Oct 2021 - March 2023",
    companyLink: "https://revature.com/",
    companyVisible: false,
  },
  {
    companyId: "GSI",
    companyName: "GSI Service Group",
    companyTitle: "Systems Specialist",
    companyDes: [
      "Constructed a Microsoft Access relational database to manage business leads and generate reports, reducing report creation time and improving user experience for business development team, cutting meeting time by 50%. ",
      "Spearheaded website enhancements, including the creation of a new career page, significantly improving user experience and engagement for hundreds of visitors. ",
      "Resolved HR-reported issues with Dayforce, updated the system with the latest HR benefits, and improved system accuracy, positively impacting over 100 employees. ",
      "Led migration of the company’s recruiting system from Dayforce to Jobvite, streamlining the recruitment process.",
      "Supported recruiting with job postings, candidate search, and newsletters increasing applicant engagement by 30%.",
    ],
    companyLink: "https://gsi-companies.com/",
    companyVisible: false,
  },
]);

const handleClick = (companyId: string) => {
  experienceObjList.value.forEach((company) => {
    if (company.companyId === companyId) {
      company.companyVisible = true;
    } else {
      company.companyVisible = false;
    }
  });
};
</script>
<style lang="css">
.experience-wrapper {
  display: block;
  text-align: left;
  padding-top: 20px;
}
.experience-nav {
  display: grid;
  grid-template-columns: 1fr 3fr;
  padding-top: 20px;
  padding-left: 45px;
}

.exp-nav-side-panel {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: flex-start;
  min-width: 225px;
}
.exp-nav-side-item {
  border: none;
  border-left: 1px solid #cecdcd;
  background-color: transparent;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  color: #3e3e3e;
  padding: 12px 4px 12px 10px;
  width: 100%;
  text-align: left;
}
.exp-nav-side-item:hover {
  color: #5cb85c;
}

.exp-nav-side-item.active {
  color: #55a855;
  background-color: #efeff0;
  border-left: 2px solid #55a855;
}

/* .exp-tab-content: {

} */
</style>
