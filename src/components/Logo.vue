<template>
  <div class="Logo">
    <h1 class="title">oleg.cloud</h1>

    <div class="social-icons">
      <a
        v-for="button in socialButtons"
        :key="button.id"
        :href="button.link"
        target="_blank"
      >
        <img
          class="icon-fade"
          :src="getImageURL(button.icon)"
          :alt="button.alt"
          :title="button.title"
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
      traits: ["learner", "intellection", "input", "analytical", "focus"],
      socialButtons: [
        {
          link: "https://www.linkedin.com/in/olegperchyk/",
          icon: "linkedin.svg",
          alt: "linkedin",
          title: "LinkedIn"
        },
        {
          link: "https://github.com/himynameisoleg",
          icon: "github.svg",
          alt: "github",
          title: "GitHub"
        },
        {
          link: "https://twitter.com/himynameisoleg",
          icon: "twitter.svg",
          alt: "twitter",
          title: "Twitter"
        },
        {
          link: "https://himynameisoleg.com",
          icon: "write.svg",
          alt: "blog",
          title: "himynameisoleg.com"
        }
      ]
    };
  },
  methods: {
    getImageURL(name) {
      return require(`../assets/icons/${name}`);
    }
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
