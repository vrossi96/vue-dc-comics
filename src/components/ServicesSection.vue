<template>
   <div id="services-section">
      <div class="container">
         <Badge v-for="(service, index) in servicesList" :key="index" :badge="service" />
      </div>
   </div>
</template>

<script>
import Badge from "./Badge.vue";

export default {
   name: "ServicesSection",
   props: ["servicesList"],
   components: {
      Badge,
   },
   data() {
      return {};
   },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_vars.scss";
@import "../assets/sass/_mixins.scss";

#services-section {
   height: 140px;
   background-color: $blue-dc;
   color: #fff;

   .container {
      @include flex_ycenter_space_around();
   }
}
</style>
