<template>
  <div id="SkillsSection">
    <div class="section-title">
      Skills
      <div class="period-style">.</div>
    </div>
    <div class="skills-wrapper fade-in">
      <div
        v-for="(skills, key) in skillsList"
        :key="key"
        class="category-wrapper"
      >
        <div class="category-name">{{ key }}</div>
        <div class="skills-items-container">
          <div class="skills-item" v-for="skill in skills">
            <i class="fa-solid fa-caret-right" />{{ skill }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
const skillsList = {
  "Programming Languages": [
    "JavaScript",
    "TypeScript",
    "Python",
    "SQL",
    "Java",
  ],
  AWS: ["S3", "Lambda", "Cloudformation", "Secrets Manager", "IAM"],
  "Frontend Technologies": [
    "Vue.js",
    "React.js",
    "D3.js",
    "HTML",
    "CSS",
    "Sass",
    "Bootstrap",
  ],
  Tools: [
    "Chrome DevTools",
    "Git",
    "Visual Studio Code",
    "Jira",
    "Figma",
    "Docker",
  ],
  "Testing Frameworks": ["Jest", "Playwright"],
};
</script>
<style lang="css" scoped>
.skills-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  width: 100%;
  margin: 0px auto;
  text-align: left;
  padding: 10px 20px 10px 40px;
}

.skills-items-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  width: 80%;
}
.skills-item {
  display: flex;
  padding: 8px;
  font-size: 15px;
  white-space: nowrap;
}

.category-name {
  font-size: 16px;
  font-weight: bold;
  padding-top: 12px;
}

.category-wrapper {
  margin-right: 40px;
}
.fa-caret-right {
  color: #198754;
  padding-top: 3px;
}

@media (max-width: 650px) {
  .skills-wrapper {
    display: grid;
    grid-template-columns: 1fr;
    padding: 10px;
  }
}
</style>
