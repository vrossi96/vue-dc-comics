<template>
   <div id="bottom-jumbo">
      <div class="container">
         <div class="card">
            <img src="../assets/img/buy-comics-digital-comics.png" alt="DC" />
            <h3>Digital comics</h3>
         </div>
         <div class="card">
            <img src="../assets/img/buy-comics-merchandise.png" alt="DC" />
            <h3>merchandise</h3>
         </div>
         <div class="card">
            <img src="../assets/img/buy-comics-shop-locator.png" alt="DC" />
            <h3>comic shop locator</h3>
         </div>
         <div class="card">
            <img src="../assets/img/buy-comics-subscriptions.png" alt="DC" />
            <h3>subscriptions</h3>
         </div>
         <div class="card">
            <img src="../assets/img/buy-dc-power-visa.svg" alt="DC" />
            <h3>dc power visa</h3>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "BottomJumbo",
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_mixins.scss";

#bottom-jumbo {
   height: 140px;
   background-color: #0282f9;
   color: #fff;

   .container {
      @include flex_ycenter_space_around();
   }

   .card {
      height: 50%;
      display: flex;
      align-items: center;
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
