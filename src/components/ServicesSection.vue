<template>
   <div id="services-section">
      <div class="container">
         <div v-for="(badge, index) in servicesList" :key="index" class="badge">
            <img :src="require(`../assets/img/${badge.img}`)" :alt="badge.name" />
            <h3>{{ badge.name }}</h3>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "ServicesSection",
   props: ["servicesList"],
   data() {
      return {};
   },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_mixins.scss";

#services-section {
   height: 140px;
   background-color: #0282f9;
   color: #fff;

   .container {
      @include flex_ycenter_space_around();
   }

   .badge {
      height: 50%;
      @include flex_center("y");
      cursor: pointer;

      img {
         height: 100%;
         padding-right: 15px;
      }

      h3 {
         text-transform: uppercase;
         font-weight: 400;
      }
   }
}
</style>
