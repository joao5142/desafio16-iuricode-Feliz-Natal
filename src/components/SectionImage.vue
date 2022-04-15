<template>
  <div class="col-md-6 container_image">
    <img class="img-fluid" v-bind:src="getImgUrl()" alt="" />
  </div>
</template>

<script>
export default {
  name: "SectionImage",
  props: {
    image: String,
  },
  data() {
    return {
      imageUrl: this.image,
    };
  },
  methods: {
    getImgUrl() {
      let image = require.context("../assets/", false, /\.svg$/);
      return image("./" + this.imageUrl);
    },
  },
};
</script>

<style scoped>
@media (max-width: 768px) {
  .container_image {
    display: flex;
    justify-content: center;
  }
}
</style>