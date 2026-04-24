<template>
  <div>
    <NavBar />
    <LandingSection />
    <AboutMeSection />
    <ExperienceSection />
    <ProjectsSection />
    <SkillsSection />
    <CertificationsSection />
    <Footer />
  </div>
</template>

<script lang="ts" setup>
import NavBar from "./components/NavBar.vue";
import LandingSection from "./components/LandingSection.vue";
import ExperienceSection from "./components/ExperienceSection.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import SkillsSection from "./components/SkillsSection.vue";
import Footer from "./components/Footer.vue";
import AboutMeSection from "./components/AboutMeSection.vue";
import CertificationsSection from "./components/CertificationsSection.vue";
import { onMounted } from "vue";

onMounted(() => {
  const elements = document.querySelectorAll(".fade-in");

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        } else {
          entry.target.classList.remove("visible");
        }
      });
    },
    { threshold: 0.1 },
  );
  elements.forEach((el) => observer.observe(el));
});
</script>

<style scoped></style>
