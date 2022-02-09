<template>
   <div id="bottom-footer">
      <div class="container">
         <div>
            <a class="sign-up" href="#">SIGN-UP NOW!</a>
         </div>
         <div class="social">
            <h2>FOLLOW US</h2>
            <a v-for="(icon, index) in social" :key="index" href="#">
               <img :src="require(`../assets/img/footer-${icon.img}.png`)" :alt="icon.name" />
            </a>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "BottomFooter",
   props: ["social"],
   data() {
      return {};
   },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_vars.scss";
@import "../assets/sass/_mixins.scss";

#bottom-footer {
   height: 120px;
   background-color: #303030;
   color: #fff;

   .container {
      @include flex_ycenter_spaced();

      .social {
         @include flex_ycenter_spaced();

         a {
            margin-left: 15px;
         }
      }
   }

   .sign-up {
      text-decoration: none;
      font-size: 25px;
      padding: 10px 20px;
      border: 2px solid $blue-dc;
      color: white;
   }

   h2 {
      font-weight: 500;
      color: $blue-dc;
      padding-right: 15px;
      padding-bottom: 5px;
   }
}
</style>
