<template>
  <main class="intro"></main>
</template>

<script>
export default {
  name: "MainIntro",
};
</script>

<style scoped>
.intro {
  background: url("../../assets/banner.png") no-repeat center center;
  width: 100%;
  background-size: cover;
  color: #fff;
  padding: 190px 0;
  text-align: center;
}

@media (max-width: 739px) {
  .intro {
    padding: 110px 0;
  }
}
</style>
