<template>
  <li class="social">
    <a href="#">
      <img v-bind:src="getImgUrl()" alt="" />
    </a>
  </li>
</template>

<script>
export default {
  name: "SocialIcon",
  props: {
    image: String,
  },
  data() {
    return {
      imageSrc: this.image,
    };
  },
  methods: {
    getImgUrl() {
      let image = require.context("../assets/", false, /\.svg$/);
      return image("./" + this.imageSrc);
    },
  },
};
</script>

<style scoped>
.social {
  background-color: var(--pink-light-color);
  position: relative;
  padding: 10px;
  border-radius: 50%;
}

@media (max-width: 450px) {
  .social {
    width: 40px;
    height: 40px;
  }
  .social img {
    width: 20px;
    height: 20px;
  }
}
</style>