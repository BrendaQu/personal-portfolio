<template>
  <div id="LandingSection" class="Landing">
    <div class="Landing-text">
      <div class="typing-text">Hi, I'm Brenda Quach.</div>
      <div style="color: #5cb85c">Software Engineer.</div>
      <div class="Landing-summary">
        Frontend-focused engineer. I build intuitive interfaces and data
        visualizations that make complexity simple. I love crafting experiences
        that feel effortless to use.
      </div>
    </div>
    <div class="Landing-img">
      <img class="profile-img" src="@/assets/pic-sticker.png" width="200px" />
    </div>
  </div>
</template>
<script lang="ts"></script>
<style lang="css">
.Landing {
  display: flex;
  flex-direction: row;
  gap: 20px;
  width: 100%;
  min-height: 870px;
  justify-content: center;
  align-items: center;
  font-size: 40px;
  text-align: center;
  flex-wrap: wrap;
}
.Landing-summary {
  font-size: 22px;
  width: 600px;
}

.Landing-text {
  width: 60%;
  min-width: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.Landing-img {
  margin: 10px;
  padding: 10px;
}

.profile-img {
  border: 2px solid #5faf5f;
  border-radius: 50%;
  box-shadow: 10px 10px 5px #c5c5c5;
}

.typing-text {
  display: inline-block;
  font-family: monospace;
  font-size: 45px;
  white-space: nowrap;
  overflow: hidden;
  border-right: 2px solid #198754; /* Green caret */
  width: 0;
  animation:
    typing 1.5s steps(10, end) forwards,
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
