<template>
  <div class="Logo">
    <h1 class="title">oleg.cloud</h1>

    <div class="social-icons">
      <a href="https://www.linkedin.com/in/olegperchyk/" target="_blank">
        <img
          class="icon-fade"
          src="../assets/icons/linkedin.svg"
          alt="linkedin"
          title="LinkedIn"
        />
      </a>
      <a href="https://github.com/himynameisoleg" target="_blank">
        <img
          class="icon-fade"
          src="../assets/icons/github.svg"
          alt="github"
          title="GitHub"
        />
      </a>
      <a href="https://twitter.com/himynameisoleg" target="_blank">
        <img
          class="icon-fade"
          src="../assets/icons/twitter.svg"
          alt="twitter"
          title="Twitter"
        />
      </a>
      <a href="https://himynameisoleg.com" target="_blank">
        <img
          class="icon-fade"
          src="../assets/icons/write.svg"
          alt="blog"
          title="himynameisoleg.com"
        />
      </a>
    </div>

    <p>
      <span class="trait" v-for="trait in traits" :key="trait.id">{{
        `${trait}.`
      }}</span>
    </p>
  </div>
</template>

<script>
export default {
  name: "Logo",
  data() {
    return {
      traits: ["learner", "intellection", "input", "analytical", "focus"]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.Logo {
  margin-top: 15vh;
}
.social-icons {
  height: 24px;
}
.icon-fade {
  animation: fadein 1s;
}
.trait {
  margin: 0 0.5em 0 0.5em;
}
img {
  margin: 0 0.5em 0 0.5em;
  &:hover {
    // cursor: pointer;
    opacity: 0.2;
    transition: opacity 0.1s ease;
  }
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
