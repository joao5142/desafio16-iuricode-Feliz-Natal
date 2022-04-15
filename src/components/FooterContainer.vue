<template>
  <footer>
    <ContainerContent>
      <div
        class="
          d-flex
          align-items-center
          justify-content-center justify-content-md-between
          flex-wrap
        "
      >
        <LogoTitle />

        <ul>
          <SocialIcon image="twitter.svg" />
          <SocialIcon image="youtube.svg" />
          <SocialIcon image="linkedin.svg" />
          <SocialIcon image="instagram.svg" />
          <SocialIcon image="facebook.svg" />
        </ul>
      </div>
    </ContainerContent>
  </footer>
</template>

<script>
import LogoTitle from "./LogoTitle.vue";
import ContainerContent from "./ContainerContent.vue";
import SocialIcon from "./SocialIcon.vue";

export default {
  name: "FooterContainer",
  components: { LogoTitle, ContainerContent, SocialIcon },
};
</script>

<style scoped>
footer {
  background-color: var(--white-color);
  padding: 40px 0px;
  display: flex;
}
ul {
  display: flex;

  gap: 40px;
}
@media (max-width: 768px) {
  ul {
    margin-top: 40px;
    justify-content: center;
    align-items: center;
  }
}

@media (max-width: 450px) {
  ul {
    gap: 20px;
    padding: 0px;
  }
}
</style>