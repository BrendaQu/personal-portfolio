<template>
  <div class="nav-wrapper">
    <a class="nav-home" @click.prevent="scrollTo('LandingSection')" href="#"
      >Brenda Quach</a
    >
    <ul class="nav nav-pills nav-items-wrapper">
      <li class="nav-item">
        <a
          :class="[
            'nav-link',
            { 'nav-active': activeSection === 'AboutMeSection' },
          ]"
          @click.prevent="scrollTo('AboutMeSection')"
          href="#"
        >
          <i class="fa-solid fa-user" />
          <div class="nav-text">About Me</div></a
        >
      </li>
      <li class="nav-item">
        <a
          :class="[
            'nav-link',
            { 'nav-active': activeSection === 'ExperienceSection' },
          ]"
          @click.prevent="scrollTo('ExperienceSection')"
          href="#"
        >
          <i class="fa-solid fa-file" />
          <div class="nav-text">Experience</div>
        </a>
      </li>
      <li class="nav-item">
        <a
          :class="[
            'nav-link',
            { 'nav-active': activeSection === 'ProjectsSection' },
          ]"
          @click.prevent="scrollTo('ProjectsSection')"
          href="#"
        >
          <i class="fa-solid fa-laptop" />
          <div class="nav-text">Projects</div>
        </a>
      </li>
      <li class="nav-item">
        <a
          :class="[
            'nav-link',
            { 'nav-active': activeSection === 'SkillsSection' },
          ]"
          @click.prevent="scrollTo('SkillsSection')"
          href="#"
        >
          <i class="fa-solid fa-gear" />
          <div class="nav-text">Skills</div>
        </a>
      </li>
      <li class="nav-item">
        <a
          :class="[
            'nav-link',
            { 'nav-active': activeSection === 'CertificationsSection' },
          ]"
          @click.prevent="scrollTo('CertificationsSection')"
          href="#"
        >
          <i class="fa-solid fa-certificate" />
          <div class="nav-text">Certifications</div>
        </a>
      </li>
    </ul>

    <div class="nav-side-links">
      <a href="https://github.com/brendaqu" target="_blank"
        ><i class="fa-brands fa-github" />
      </a>
      <a href="https://www.linkedin.com/in/brenda-qu" target="_blank">
        <i class="fa-brands fa-linkedin" />
      </a>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { ref, onMounted } from "vue";
const activeSection = ref("");

onMounted(() => {
  const sections = document.querySelectorAll(
    "#LandingSection, #AboutMeSection, #ExperienceSection, #ProjectsSection, #SkillsSection, #CertificationsSection",
  );

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          activeSection.value = entry.target.id;
        }
      });
    },
    { threshold: 0, rootMargin: "-50% 0px -50% 0px" },
  );

  sections.forEach((section) => observer.observe(section));
});

const scrollTo = (id: string) => {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
};
</script>
<style lang="css">
.nav-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  position: sticky;
  z-index: 1000;
  top: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
}

.nav-active {
  color: #55a855 !important;
}
.nav-home {
  text-decoration: none !important;
  color: #111827;
  font-size: 24px;
  font-weight: bold;
  padding: 2px;
  margin-left: 20px;
  margin-right: 10px;
  min-width: 170px;
}

.nav-side-links {
  margin-right: 20px;
  margin-left: 10px;
  min-width: 40px;
}

.nav-link {
  display: flex !important;
  justify-content: center !important;
  align-items: center !important;
  flex-direction: row;
  width: 100%;
}

@media (max-width: 860px) {
  .nav-text {
    display: none;
  }
  .nav-link {
    padding: 5px !important;
  }
  .fa-solid {
    margin-right: 0px !important;
  }
}

@media (max-width: 471px) {
  .nav-home {
    font-size: 16px;
    min-width: 130px;
  }
  .fa-brands {
    font-size: 12px !important;
  }
  .nav-link {
    padding: 3px !important;
  }
  .fa-solid {
    font-size: 12px !important;
  }
}

.nav-side-links a {
  color: black;
}
.nav-items-wrapper {
  font-size: 14px;
  min-width: 115px;
  gap: 0px;
  font-weight: bold;
  border: 1px solid #f2f2f2;
  background-color: #e7e7e8;
  border-radius: 20px;
  padding-right: 5px;
  padding-left: 5px !important;
}

.nav-item a {
  color: #3e3e3e;
  padding: 8px;
  margin: 2px;
}
.nav-item a:hover {
  color: #5cb85c !important;
}
.nav-item a:focus {
  outline: none;
  color: inherit;
}

.fa-solid {
  margin-right: 5px;
}
.fa-brands {
  font-size: 24px;
  margin-right: 5px;
  color: #5cb85c;
}

.fa-brands:hover {
  color: black;
}
</style>
