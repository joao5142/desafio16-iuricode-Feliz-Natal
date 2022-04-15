<template>
  <button>
    <img src="../assets/gift.svg" alt="" />
    <p>{{ buttonTitle }}</p>
  </button>
</template>

<script>
export default {
  name: "ButtonDonate",
  props: {
    title: String,
  },
  data() {
    return {
      buttonTitle: this.title,
    };
  },
};
</script>

<style scoped>
* {
  margin: 0px;
  padding: 0px;
}
button {
  padding: 8px 30px;
  border-radius: 10px;
  background-color: var(--red-color);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  margin-top: 30px;
}
p {
  color: var(--white-color);
  font-size: 0.9rem;
}
button:active {
  transform: scale(98%);
}
button:hover img {
  animation: rotate 0.7s linear infinite;
}

@keyframes rotate {
  100% {
    transform: translateY(-10px);
  }
}
</style>