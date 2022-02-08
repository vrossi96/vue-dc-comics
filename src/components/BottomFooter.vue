<template>
   <div id="bottom-footer">
      <div class="container">
         <h2>Content Goes Here</h2>
      </div>
   </div>
</template>

<script>
export default {
   name: "BottomFooter",
};
</script>

<style scoped lang="scss">
#bottom-footer {
   height: 120px;
   background-color: #303030;
   color: #fff;

   .container {
      display: flex;
      align-items: center;
   }
}
</style>
