<template>
  <header class="header center">
    <Logo />
    <nav class="header__navigation">
      <Navigation />
    </nav>
  </header>
</template>

<script>
import Navigation from "./Navigation.vue";
import Logo from "./Logo.vue";

export default {
  name: "AppHeader",
  components: {
    Navigation,
    Logo,
  },
  props: {},
};
</script>

<style scoped lang="scss">
.navlist {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 48px;
}
.header__navigation :deep(.navlist__item-link) {
  color: #292f36;
  text-align: center;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 125%;
  transition: 0.3s;
  &:hover {
    color: #cda274;
  }
}
</style>
