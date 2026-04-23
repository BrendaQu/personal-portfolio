<template>
  <Transition name="fade">
    <div v-if="cardVisible" class="card-wrapper">
      <div class="card-grouping-1">
        <div class="card-company-title">{{ cardCompanyTitle }}</div>
        <div class="card-company">
          <a :href="cardCompanyLink" target="_blank">@ {{ cardCompany }}</a>
        </div>
      </div>
      <div class="card-years-active">{{ cardCompanyYears }}</div>
      <div v-for="item in cardCompanyDescription" class="card-company-desc">
        <i class="fa-solid fa-caret-right" />
        <div>{{ item }}</div>
      </div>
    </div>
  </Transition>
</template>
<script lang="ts" setup>
defineProps<{
  cardCompany: string;
  cardCompanyYears: string;
  cardCompanyTitle: string;
  cardCompanyDescription: string[];
  cardCompanyLink: string;
  cardVisible: boolean;
}>();
</script>
<style lang="css" scoped>
.card-wrapper {
  text-align: left;
  display: flex;
  flex-direction: column;
  color: #111827;
  width: 100%;
  min-width: 330px;
  min-height: 450px;
}

.card-grouping-1 {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}
.card-company {
  font-size: 20px;
  font-weight: bold;
  color: #55a855;
  position: relative;
}

.card-company a {
  text-decoration: none !important;
  color: #55a855;
}

.card-company::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 25px;
  width: 0;
  height: 1px;
  background-color: #55a855;
  transition: width 0.3s ease;
}

.card-company:hover::after {
  width: 92%;
}

.card-company-title {
  font-size: 20px;
  font-weight: bold;
  padding-right: 8px;
}

.card-company-desc {
  display: flex;
  gap: 8px;
  font-size: 16px;
  padding: 6px;
}

.card-years-active {
  font-size: 18px;
  padding-bottom: 10px;
}

.fa-caret-right {
  color: #198754;
  padding-top: 4px;
}

.fade-enter-active {
  transition: opacity 1s ease;
}

.fade-enter-from {
  opacity: 0;
}
</style>
