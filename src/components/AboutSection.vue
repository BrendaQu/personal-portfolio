<template>
  <div id="AboutSection" class="about-me">
    <div class="about-me-text">
      <div class="typing-text">Hi, I'm Brenda Quach.</div>
      <div style="color: #5cb85c">Software Engineer.</div>
      <div class="about-summary">
        Frontend-focused engineer. I build intuitive interfaces and data
        visualizations that make complexity simple. I love crafting experiences
        that feel effortless to use.
      </div>
    </div>
    <div class="about-me-img">
      <img src="@/assets/pic-sticker.png" width="200px" />
    </div>
  </div>
</template>
<script lang="ts"></script>
<style lang="css">
.about-me {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: auto;
  justify-content: center;
  align-items: center;
  font-size: 32px;
  text-align: center;
  flex-wrap: wrap;
}
.about-summary {
  font-size: 18px;
  width: 400px;
}

.about-me-text {
  width: 50%;
  min-width: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.about-me-img {
  margin: 20px;
  padding: 20px;
}

.typing-text {
  display: inline-block;
  font-family: monospace;
  white-space: nowrap;
  overflow: hidden;
  border-right: 2px solid #198754; /* Green caret */
  width: 0;
  animation: typing 1.5s steps(10, end) forwards,
    blink 0.6s step-end infinite alternate;
}

@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 20ch;
  } /* adjust '20ch' to match your text length */
}

@keyframes blink {
  50% {
    border-color: transparent;
  }
}
</style>
