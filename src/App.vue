<template>
   <div id="App">
      <Header />
      <Jumbotron />
      <ServicesSection />
      <TopFooter />
      <BottomFooter />
   </div>
</template>

<script>
import Header from "./components/Header.vue";
import Jumbotron from "./components/Jumbotron.vue";
import ServicesSection from "./components/ServicesSection.vue";
import TopFooter from "./components/TopFooter.vue";
import BottomFooter from "./components/BottomFooter.vue";

export default {
   name: "App",
   components: {
      Header,
      Jumbotron,
      ServicesSection,
      TopFooter,
      BottomFooter,
   },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
