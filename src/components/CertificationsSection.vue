<template>
  <div id="CertificationsSection">
    <div class="section-title">
      Certifications
      <div class="period-style">.</div>
    </div>
    <div class="certifications-wrapper">
      <a
        class="cert-card"
        href="https://www.credly.com/badges/dea3424f-39e0-4280-90c5-32ea8c5a4fe9/public_url"
        target="_blank"
      >
        <img
          class="cert-img"
          src="@/assets/aws-certified-developer-associate.png"
        />
      </a>
      <a
        class="cert-card"
        href="https://www.credly.com/badges/970a77eb-aac5-44d7-84b2-48893644277f/public_url"
        target="_blank"
      >
        <img
          class="cert-img"
          src="@/assets/aws-certified-ai-practitioner.png"
        />
      </a>
      <a
        class="cert-card"
        href="https://www.credly.com/badges/e3f5420d-5f22-4d5f-840b-a5168f3e9495/public_url"
        target="_blank"
      >
        <img
          class="cert-img"
          src="@/assets/aws-certified-cloud-practitioner.png"
        />
      </a>
    </div>
  </div>
</template>
<script lang="ts" setup></script>
<style lang="css">
.certifications-wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-start;
  padding: 30px;
  margin-left: 30px;
  gap: 30px;
  min-height: 350px;
}

.cert-card {
  padding: 8px;
}
.cert-img {
  width: 150px;
}

.cert-card:hover {
  transform: scale(1.05);
  transition: transform 0.3s ease;
}
</style>
