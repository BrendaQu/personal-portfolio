<template>
  <div class="nav-wrapper">
    <div class="nav-home">Brenda Quach</div>
    <ul class="nav nav-pills nav-items-wrapper">
      <li class="nav-item">
        <a class="nav-link" href="#"> <i class="fa-solid fa-user" />About Me</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">
          <i class="fa-solid fa-file" />Experience</a
        >
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">
          <i class="fa-solid fa-laptop" />Projects</a
        >
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#"> <i class="fa-solid fa-gear"></i>Skills</a>
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
}

.nav-home {
  font-size: 24px;
  font-weight: bold;
  padding: 2px;
  margin-left: 20px;
}

.nav-side-links {
  margin-right: 20px;
}

.nav-side-links a {
  color: black;
}
.nav-items-wrapper {
  display: flex;
  font-size: 18px;
  gap: 10px;
  font-weight: 500;
  border: 1px solid #f2f2f2;
  background-color: #f2f2f2;
  border-radius: 20px;
}

.nav-item a {
  color: gray;
}
a:hover {
  color: black !important;
}

.fa-solid {
  margin-right: 5px;
}
.fa-brands {
  font-size: 24px;
  margin-right: 5px;
}
</style>
