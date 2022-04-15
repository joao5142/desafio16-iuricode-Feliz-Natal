<template>
  <div class="col-md-6 donate_card">
    <p class="title">{{ cardTitle }}</p>
    <p>
      {{ cardText }}
    </p>
    <ButtonDonate v-bind:title="buttonTitle" />
  </div>
</template>

<script>
import ButtonDonate from "./ButtonDonate.vue";

export default {
  name: "DonateCard",
  props: {
    title: String,
    text: String,
    btnTitle: String,
  },
  data() {
    return {
      cardTitle: this.title,
      cardText: this.text,
      buttonTitle: this.btnTitle,
    };
  },
  components: { ButtonDonate },
};
</script>

<style scoped>
.donate_card {
  padding-right: 200px;
}

@media (max-width: 975px) {
  .donate_card {
    padding-right: 0px;
  }
}
</style>