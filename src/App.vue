<template>
  <ContainerContent>
    <NavHead />
  </ContainerContent>
  <MainContainer />
  <FooterContainer />
</template>

<script>
import NavHead from "./components/NavHead.vue";
import MainContainer from "./components/MainContainer.vue";
import ContainerContent from "./components/ContainerContent.vue";
import FooterContainer from "./components/FooterContainer.vue";

export default {
  name: "App",
  components: { NavHead, MainContainer, ContainerContent, FooterContainer },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap");

/*##RESET*/
* {
  box-sizing: border-box;
  padding: 0px;
  margin: 0px;
}

ul,
ol {
  list-style: none;
}

a {
  text-decoration: none;
}

img {
  height: auto;
}

button,
input,
textarea {
  border: 0;
  outline: none;
}

button:focus,
input:focus,
textarea:focus {
  border: 0;
  outline: none;
}

body {
  font-family: "Poppins", sans-serif;
  background-color: var(--pink-color);
  font-weight: 500;
  color: var(--black-light-color);
  overflow-x: hidden;
}
/*##UTILS */
.title {
  font-size: 3rem;
  font-weight: 600;
  letter-spacing: 0.2px;
}
/*##VARIAVEIS*/
:root {
  --red-color: #da2535;
  --pink-color: #f7c7b9;
  --pink-light-color: #f4d9dc;
  --white-color: #f9f9f9;
  --gray-200-color: #404040;
  --gray-color: #8d8d8d;
  --black-light-color: #161212;
}
</style>
