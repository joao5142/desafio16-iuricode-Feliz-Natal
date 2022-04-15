<template>
  <div class="col-md-3 acessorie">
    <img v-bind:src="getImgUrl()" />
    <p>{{ cardTitle }}</p>
    <p class="text">{{ cardText }}</p>
  </div>
</template>

<script>
export default {
  name: "AcessorieCard",
  props: {
    title: String,
    image: String,
    text: String,
  },
  data() {
    return {
      cardTitle: this.title,
      cardImage: this.image,
      cardText: this.text,
    };
  },
  methods: {
    getImgUrl() {
      let image = require.context("../assets/", false, /\.svg$/);
      return image("./" + this.cardImage);
    },
  },
};
</script>

<style scoped>
.acessorie {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
p {
  text-align: center;
}
.text {
  font-size: 0.9rem;
  color: var(--gray-color);
}
</style>