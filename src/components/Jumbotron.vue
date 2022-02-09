<template>
   <div id="jumbotron">
      <div class="jumbo-top-bg"></div>
      <div class="container">
         <div class="label">
            <h2>Current series</h2>
         </div>
         <!-- CARDS HERE -->
         <div v-if="comicsList.length" class="card-container">
            <Card v-for="comicCard in comicsList" :key="comicCard.series" :comic="comicCard" />
         </div>
         <div class="button-cont">
            <a class="button" href="#">load more</a>
         </div>
      </div>
   </div>
</template>

<script>
import Card from "./Card.vue";

export default {
   name: "Jumbotron",
   props: ["comicsList"],
   components: {
      Card,
   },
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
   }
}
</style>
