<template>
  <div class="nav-wrapper">
    <div class="nav-home">Brenda Quach</div>
    <ul class="nav nav-pills nav-items-wrapper">
      <li class="nav-item">
        <a class="nav-link" href="#AboutSection">
          <i class="fa-solid fa-user" />
          <div class="nav-text">About Me</div></a
        >
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#ExperienceSection">
          <i class="fa-solid fa-file" />
          <div class="nav-text">Experience</div>
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#ProjectsSection">
          <i class="fa-solid fa-laptop" />
          <div class="nav-text">Projects</div>
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#SkillsSection">
          <i class="fa-solid fa-gear" />
          <div class="nav-text">Skills</div>
        </a>
      </li>
    </ul>

    <div class="nav-side-links">
      <a href="https://github.com/brendaqu" target="_blank"
        ><i class="fa-brands fa-github" />
      </a>
      <a
        href="https://www.linkedin.com/in/brenda-q-50778617a/"
        c
        target="_blank"
      >
        <i class="fa-brands fa-linkedin" />
      </a>
    </div>
  </div>
</template>
<script lang="ts"></script>
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
  background-color: white;
}

.nav-home {
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

@media (max-width: 790px) {
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

@media (max-width: 437px) {
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
  gap: 5px;
  font-weight: bold;
  border: 1px solid #f2f2f2;
  background-color: #e7e7e8;
  border-radius: 20px;
  padding-right: 5px;
  padding-left: 5px !important;
}

.nav-item a {
  color: #3e3e3e;
}
a:hover {
  color: #5cb85c !important;
}
a:focus {
  color: #5cb85c !important;
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
