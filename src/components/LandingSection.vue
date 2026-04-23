<template>
  <div id="LandingSection" class="Landing">
    <div class="Landing-text">
      <div class="typing-text">Hi, I'm Brenda Quach.</div>
      <div class="landing-subtitle" style="color: #5cb85c">
        Software Engineer.
      </div>
      <div class="Landing-summary">
        Frontend-focused engineer specializing in data visualizations and
        interactive interfaces. I turn complex data into experiences that feel
        effortless to use.
      </div>
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
  min-height: 500px;
  justify-content: center;
  align-items: center;
  font-size: 40px;
  text-align: center;
  flex-wrap: wrap;
}
.Landing-summary {
  font-size: 22px;
}

.Landing-text {
  width: 60%;
  min-width: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
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

.Landing-summary {
  animation: fadeUp 1s ease 2.5s both;
}
.landing-subtitle {
  animation: fadeUp 1s ease 1.7s both;
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

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 515px) {
  .Landing {
    font-size: 40px;
  }
  .typing-text {
    font-size: 40px;
  }
  .Landing-summary {
    font-size: 18px;
  }
}

@media (max-width: 475px) {
  .Landing {
    font-size: 35px;
  }
  .typing-text {
    font-size: 35px;
  }
  .Landing-summary {
    font-size: 16px;
  }
}

@media (max-width: 415px) {
  .Landing {
    font-size: 30px;
  }
  .typing-text {
    font-size: 30px;
  }
  .Landing-summary {
    font-size: 14px;
  }
}
</style>
