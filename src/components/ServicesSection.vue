<template>
   <div id="services-section">
      <div class="container">
         <div v-for="(badge, index) in services" :key="index" class="badge">
            <img :src="require(`../assets/img/${badge.img}`)" :alt="badge.name" />
            <h3>{{ badge.name }}</h3>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "ServicesSection",
   data() {
      return {
         services: [
            { name: "Digital comics", img: "buy-comics-digital-comics.png" },
            { name: "merchandise", img: "buy-comics-merchandise.png" },
            { name: "comic shop locator", img: "buy-comics-shop-locator.png" },
            { name: "subscriptions", img: "buy-comics-subscriptions.png" },
            { name: "dc power visa", img: "buy-dc-power-visa.svg" },
         ],
      };
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
