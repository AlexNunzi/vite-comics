<script>

import TheHeader from "./components/TheHeader.vue";
import Navigation from "./components/Navigation.vue";
import FooterLinks from "./components/TheFooterLinks.vue";

export default{
  components:{
    TheHeader,
    Navigation,
    FooterLinks,
  }
}
</script>

<template>

<TheHeader />

<main>
  <div class="main-content container d-flex align-center">
    <h1>Content goes hear</h1>
  </div>
</main>

<Navigation />

<FooterLinks />

</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
