<template>
  <ul>
    <li>
      <a href="#">Início</a>
    </li>
    <li>
      <a href="#">Acessórios</a>
    </li>
    <li>
      <a href="#">Doação</a>
    </li>
    <li>
      <a href="#">Contato</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "NavList",
};
</script>

<style scoped>
* {
  margin: 0px;
  padding: 0px;
}
nav {
  padding-top: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
ul {
  display: flex;
  gap: 30px;
  align-items: center;
}
a {
  color: var(--black-light-color);
  font-size: 0.9rem;
}
li {
  position: relative;
}
li::before {
  content: "";
  width: 0%;
  height: 2px;
  background-color: var(--red-color);
  position: absolute;
  bottom: -2px;
  transform-origin: center;
}
li:hover::before {
  width: 100%;
  animation: grow 0.6s linear;
}

@keyframes grow {
  0% {
    transform: scaleX(0);
  }

  100% {
    transform: scaleX(1);
  }
}
</style>