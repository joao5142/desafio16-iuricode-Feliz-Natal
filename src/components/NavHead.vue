<template>
  <header>
    <nav>
      <LogoTitle />
      <NavList v-if="!isActive" class="d-none d-sm-flex" />
      <img
        v-on:click="showMenu()"
        src="../assets/bars.svg"
        class="d-block d-sm-none hamburguer"
      />
    </nav>
    <NavList class="mobile_nav" v-if="isActive" />
  </header>
</template>

<script>
import LogoTitle from "./LogoTitle.vue";
import NavList from "./NavList.vue";

export default {
  name: "NavHead",
  components: {
    LogoTitle,
    NavList,
  },
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    showMenu() {
      this.isActive = !this.isActive;
      console.log(this.isActive);
    },
  },
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
.hamburguer {
  width: 32px;
  cursor: pointer;
}
.mobile_nav {
  margin-top: 20px;
  justify-content: center;
}
</style>