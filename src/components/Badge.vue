<template>
   <div class="badge">
      <img :src="require(`../assets/img/${badge.img}`)" :alt="badge.name" />
      <h3>{{ badge.name }}</h3>
   </div>
</template>

<script>
export default {
   name: "Badge",
   props: ["badge"],
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_mixins.scss";

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
</style>
