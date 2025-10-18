<template>
  <div class="card-wrapper">
    <div class="card-grouping-1">
      <div class="card-company">{{ cardCompany }}</div>
      <div class="card-years-active">{{ cardCompanyYears }}</div>
    </div>
    <div class="card-company-title">{{ cardCompanyTitle }}</div>
    <div class="card-company-desc">
      {{ cardCompanyDescription }}
    </div>
  </div>
</template>
<script lang="ts" setup>
defineProps<{
  cardCompany: string;
  cardCompanyYears: string;
  cardCompanyTitle: string;
  cardCompanyDescription: string;
}>();
</script>
<style lang="css" scoped>
.card-wrapper {
  text-align: left;
  display: flex;
  flex-direction: column;
  margin: 15px 20px;
  padding: 20px;
  color: #111827;
  border: 1px solid #e6dcc6;
  border-radius: 10px;
  background-color: #a4cb9d;
  min-width: 280px;
}

.card-grouping-1 {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
.card-company {
  font-size: 20px;
  font-weight: bold;
}

.card-company-title {
  font-style: italic;
  font-size: 18px;
}

.card-company-desc {
  font-size: 16px;
}

.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.6s ease;
}

.fade-in.show {
  opacity: 1;
  transform: translateY(0);
}
</style>
