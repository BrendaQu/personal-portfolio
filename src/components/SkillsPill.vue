<template>
  <div class="pill-wrapper">{{ pillSkillName }}</div>
</template>
<script lang="ts" setup>
defineProps<{
  pillSkillName: string;
}>();
</script>
<style lang="css">
.pill-wrapper {
  display: inline-block;
  width: max-content;
  border: 1px solid #f2f2f2;
  border-radius: 10px;
  padding: 4px 15px;
  color: #5cb85c;
  font-weight: bold;
  font-size: 18px;
  background-color: #e7e7e8;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.pill-wrapper:hover {
  transform: translateY(-4px) scale(1.05);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}

@keyframes wave {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-5px);
  }
}
</style>
