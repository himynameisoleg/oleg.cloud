<template>
  <div class="Logo">
    <h1>oleg.cloud</h1>
    <a href="https://www.linkedin.com/in/olegperchyk/" target="_blank">
      <img src="../assets/icons/linkedin.svg" />
    </a>
    <a href="https://github.com/himynameisoleg" target="_blank">
      <img src="../assets/icons/github.svg" />
    </a>
    <a href="https://twitter.com/himynameisoleg" target="_blank">
      <img src="../assets/icons/twitter.svg" />
    </a>

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
</style>
