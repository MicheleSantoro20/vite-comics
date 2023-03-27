<script >
  import TheHeader from "./components/TheHeader.vue";
  import MainContent from "./components/MainContent.vue";
  import MainNavBar from "./components/MainNavBar.vue";

  export default {
    components: {
      TheHeader,
      MainContent,
      MainNavBar,
    }
  }
</script>

<template>

  <TheHeader />
  <MainContent />
  <MainNavBar />

</template>

<style lang="scss">
@use "./styles/general.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Roboto Condensed', sans-serif;
}
</style>
