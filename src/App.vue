<template>
   <div id="App">
      <Header />
      <TopJumbo />
   </div>
</template>

<script>
import Header from "./components/Header.vue";
import TopJumbo from "./components/TopJumbo.vue";

export default {
   name: "App",
   components: {
      Header,
      TopJumbo,
   },
};
</script>

<style lang="scss">
* {
   margin: 0;
   padding: 0;
   box-sizing: border-box;
}
body {
   font-family: Avenir, Helvetica, Arial, sans-serif;
   height: 100vh;
}
img {
   max-width: 100%;
   height: auto;
}

.container {
   width: 100%;
   height: 100%;
   max-width: 1200px;
   margin: 0 auto;
}
</style>
