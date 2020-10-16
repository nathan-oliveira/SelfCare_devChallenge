<template>
  <router-view />
</template>

<script>
export default {
  name: "app",
  components: {},
};
</script>

<style lang="scss">
@import url(https://fonts.googleapis.com/css2?family=Lato:wght@400;900&display=swap);
@import url(https://fonts.googleapis.com/css2?family=Cabin:wght@400;600;700&display=swap);
@import "./styles/reset.css";

$fa-font-path: "~@fortawesome/fontawesome-free/webfonts";
@import "~@fortawesome/fontawesome-free/scss/fontawesome";
@import "~@fortawesome/fontawesome-free/scss/solid";
// @import "~@fortawesome/fontawesome-free/scss/regular";
// @import "~@fortawesome/fontawesome-free/scss/brands";
</style>
