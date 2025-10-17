<template>
  <div class="card-wrapper">
    <div class="card-grouping-1">
      <div class="card-company">{{ cardCompany }}</div>
      <div class="card-years-active">{{ cardCompanyYears }}</div>
    </div>
    <div class="card-company-title">{{ cardCompanyTitle }}</div>
    <div class="card-company-desc">{{ cardCompanyDescription }}</div>
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
  color: black;
  border: 1px solid lightgray;
  border-radius: 10px;
  background-color: #ededeb;
}

.card-grouping-1 {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
.card-company {
  font-size: 24px;
}

.card-company-title {
  font-style: italic;
  font-size: 18px;
}

.card-company-desc {
  font-size: 15px;
}
</style>
