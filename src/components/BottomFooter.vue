<template>
   <div id="bottom-footer">
      <div class="container">
         <div>
            <a class="sign-up" href="#">SIGN-UP NOW!</a>
         </div>
         <div class="social">
            <h2>FOLLOW US</h2>
            <a v-for="logo in social" :key="logo.name" href="#">
               <img :src="`../assets/img/${logo.img}.png`" :alt="logo.name" />
            </a>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "BottomFooter",
   data() {
      return {
         social: [
            { name: "facebook", img: "facebook" },
            { name: "periscope", img: "periscope" },
            { name: "pinterest", img: "pinterest" },
            { name: "twitter", img: "twitter" },
            { name: "youtube", img: "youtube" },
         ],
      };
   },
};
</script>

<style scoped lang="scss">
#bottom-footer {
   height: 120px;
   background-color: #303030;
   color: #fff;

   .container {
      display: flex;
      justify-content: space-between;
      align-items: center;

      .social {
         display: flex;
         justify-content: space-between;
         align-items: center;
      }
   }

   .sign-up {
      text-decoration: none;
      font-size: 25px;
      padding: 10px 20px;
      border: 2px solid #0282f9;
      color: white;
   }

   h2 {
      font-weight: 500;
      color: #0282f9;
      padding-right: 15px;
   }
}
</style>
