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
  padding: 3px 10px;
  color: #5cb85c;
  font-weight: bold;
  font-size: 16px;
  background-color: #e7e7e8;
}
</style>
