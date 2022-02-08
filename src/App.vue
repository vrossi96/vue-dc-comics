<template>
   <div id="App">
      <Header />
      <TopJumbo />
      <BottomJumbo />
      <TopFooter />
      <BottomFooter />
   </div>
</template>

<script>
import Header from "./components/Header.vue";
import TopJumbo from "./components/TopJumbo.vue";
import BottomJumbo from "./components/BottomJumbo.vue";
import TopFooter from "./components/TopFooter.vue";
import BottomFooter from "./components/BottomFooter.vue";

export default {
   name: "App",
   components: {
      Header,
      TopJumbo,
      BottomJumbo,
      TopFooter,
      BottomFooter,
   },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
