<template>
  <div @click="handleClick">
    <div class="project-card-wrapper">
      <div class="project-heading-group">
        <div class="project-card-title">{{ projectTitle }}</div>
        <div>
          <i class="fa-solid fa-arrow-up-right-from-square"></i>
        </div>
      </div>
      <div class="project-card-description">{{ projectDescription }}</div>
    </div>
  </div>
</template>
<script lang="ts" setup>
const props = defineProps<{
  projectTitle: string;
  projectLink: string;
  projectDescription: string;
}>();
const handleClick = () => {
  window.open(props.projectLink);
};
</script>
<style lang="css" scoped>
.project-card-wrapper {
  width: 300px;
  height: 200px;
  border: 1px solid #e6dcc6;
  border-radius: 10px;
  background-color: #a4cb9d;
  color: #111827;
  padding: 22px;
  margin: 20px;
  cursor: pointer;
  text-align: left;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card-wrapper:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

.project-heading-group {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.project-card-wrapper:hover {
  color: #e7e7e8;
}

.project-card-title {
  font-size: 20px;
  font-weight: bold;
}

.project-card-description {
  font-size: 16px;
  padding-top: 25px;
}

.fa-solid {
  font-size: 20px;
}
</style>
