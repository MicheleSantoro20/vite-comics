<script >
  import TheHeader from "./components/TheHeader.vue";
  import MainContent from "./components/MainContent.vue";

  export default {
    components: {
      TheHeader,
      MainContent,
    }
  }
</script>

<template>

  <TheHeader />
  <MainContent />

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
