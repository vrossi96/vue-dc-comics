<template>
   <div id="bottom-footer">
      <div class="container">
         <div>
            <a class="sign-up" href="#">SIGN-UP NOW!</a>
         </div>
         <div class="social">
            <h2>FOLLOW US</h2>
            <a href="#">
               <img src="../assets/img/footer-facebook.png" alt="facebook" />
            </a>
            <a href="#">
               <img src="../assets/img/footer-periscope.png" alt="periscope" />
            </a>
            <a href="#">
               <img src="../assets/img/footer-pinterest.png" alt="pinterest" />
            </a>
            <a href="#">
               <img src="../assets/img/footer-twitter.png" alt="twitter" />
            </a>
            <a href="#">
               <img src="../assets/img/footer-youtube.png" alt="youtube" />
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

         a {
            margin-left: 15px;
         }
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
      padding-bottom: 5px;
   }
}
</style>
