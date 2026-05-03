<template>
  <div>
    <div class="project-card-wrapper">
      <div>
        <img
          class="project-img"
          :src="getImgUrl(projectImg)"
          width="100%"
          height="220px"
        />
      </div>
      <div class="project-heading-group">
        <div class="project-card-title">{{ projectTitle }}</div>
        <div>
          <i class="fa-brands fa-github" @click="handleClickGithub" />
          <i
            v-if="projectLink !== ''"
            class="fa-solid fa-arrow-up-right-from-square"
            @click="handleClickLink"
          ></i>
        </div>
      </div>
      <div class="project-card-description">{{ projectDescription }}</div>
      <div class="project-card-tech-section">
        <div v-for="skill in projectSkills" class="project-card-tech-item">
          <SkillsPill :pillSkillName="skill" />
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import SkillsPill from "./SkillsPill.vue";
const props = defineProps<{
  projectTitle: string;
  projectLink: string;
  projectGithub: string;
  projectDescription: string;
  projectSkills: string[];
  projectImg: string;
}>();
const handleClickLink = () => {
  window.open(props.projectLink);
};
const handleClickGithub = () => {
  window.open(props.projectGithub);
};

const getImgUrl = (img: string) => {
  return new URL(`../assets/${img}`, import.meta.url).href;
};
</script>
<style lang="css" scoped>
.project-card-wrapper {
  width: 370px;
  height: 430px;
  border-radius: 5px;
  background-color: #e7e7e8;
  color: #111827;
  padding: 20px;
  margin: 10px;
  text-align: left;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.project-card-wrapper:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

.project-heading-group {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 10px;
}

.project-card-wrapper:hover {
  .project-img {
    opacity: 1;
    filter: grayscale(0%);
  }
}

.project-card-title {
  font-size: 20px;
  font-weight: bold;
  font-family: Arial, Helvetica, sans-serif;
}

.project-card-description {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  padding-top: 12px;
}

.project-img {
  border-radius: 5px;
  width: 100%;
  height: 200px;
  object-fit: cover;
  object-position: top;
  opacity: 0.7;
  filter: grayscale(90%);
}

.fa-solid {
  font-size: 20px;
}

.project-card-tech-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: left;
  padding-top: 5px;
}

.project-card-tech-item {
  display: flex;
  flex-direction: row;
  padding-right: 4px;
  padding-top: 4px;
}
.fa-solid {
  margin-right: 5px;
}
.fa-brands {
  font-size: 21px;
  margin-right: 5px;
  color: black;
}

.fa-github:hover,
.fa-arrow-up-right-from-square:hover {
  color: #5cb85c;
  cursor: pointer;
}
</style>
