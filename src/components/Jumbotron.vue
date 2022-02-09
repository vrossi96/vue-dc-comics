<template>
   <div id="jumbotron">
      <div class="jumbo-top-bg"></div>
      <div class="container">
         <div class="label">
            <h2>Current series</h2>
         </div>
         <!-- CARDS HERE -->
         <div class="card-container">
            <div v-for="card in comicsList" :key="card.series" class="card">
               <a href="#">
                  <div class="pic">
                     <img :src="card.thumb" :alt="card.series" />
                  </div>
                  <p>{{ card.series }}</p>
               </a>
            </div>
         </div>
         <div class="button-cont">
            <a class="button" href="#">load more</a>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: "Jumbotron",
   props: ["comicsList"],
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_mixins.scss";

#jumbotron {
   background-color: #1c1c1c;
   color: #fff;

   .jumbo-top-bg {
      height: 500px;
      background-image: url(../assets/img/jumbotron.jpg);
      background-position: center top;
   }
   .container {
      padding: 30px 0;
      position: relative;

      .label {
         position: absolute;
         top: 0;
         left: 0;
         transform: translateY(-50%);
         padding: 10px 25px;
         background-color: #0282f9;

         h2 {
            text-transform: uppercase;
         }
      }
      .button-cont {
         @include flex_center("x");

         .button {
            padding: 10px 75px;
            background-color: #0282f9;
            display: inline-block;
         }
      }

      a {
         text-decoration: none;
         color: #fff;
         text-transform: uppercase;
      }
      // *****************CARDS
      .card-container {
         width: 100%;
         @include flex_center("y");
         flex-wrap: wrap;
      }
      .card {
         width: calc(100% / 6 - 30px);
         height: 260px;
         margin: 20px 15px;

         .pic {
            height: 190px;
            width: 100%;
            overflow: hidden;
            margin-bottom: 20px;
         }

         p {
            text-transform: uppercase;
         }
      }
   }
}
</style>
