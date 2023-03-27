<script >
  import TheHeader from "./components/TheHeader.vue";
  import MainContent from "./components/MainContent.vue";
  import MainNavBar from "./components/MainNavBar.vue";
  import FooterSection from "./components/FooterSection.vue";
  import SignUpAndSocial from "./components/SignUpAndSocial.vue";

  export default {
    components: {
      TheHeader,
      MainContent,
      MainNavBar,
      FooterSection,
      SignUpAndSocial,
    }
  }
</script>

<template>

  <TheHeader />
  <MainContent />
  <MainNavBar />
  <FooterSection />
  <SignUpAndSocial />

</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
