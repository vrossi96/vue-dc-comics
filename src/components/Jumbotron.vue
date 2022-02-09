<template>
   <div id="jumbotron">
      <div class="jumbo-top-bg"></div>
      <div class="container">
         <h2>Content Goes Here</h2>
      </div>
   </div>
</template>

<script>
export default {
   name: "Jumbotron",
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_mixins.scss";

#jumbotron {
   height: 900px;
   background-color: #1c1c1c;
   color: #fff;

   .container {
      height: 55%;
      display: flex;
      align-items: center;
      @include flex_center("y");
   }
   .jumbo-top-bg {
      height: 45%;
      background-image: url(../assets/img/jumbotron.jpg);
   }
}
</style>
