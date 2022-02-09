<template>
   <div class="card">
      <a href="#">
         <div class="pic">
            <img :src="comic.thumb" :alt="comic.series" />
         </div>
         <p>{{ comic.series }}</p>
      </a>
   </div>
</template>

<script>
export default {
   name: "Card",
   props: ["comic"],
};
</script>

<style scoped lang="scss">
a {
   text-decoration: none;
   color: #fff;
   text-transform: uppercase;
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
</style>
