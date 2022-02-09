<template>
   <header>
      <nav class="container">
         <!-- Left part with logo -->
         <div><img src="../assets/img/dc-logo.png" alt="DC Logo" /></div>
         <!-- Right part with list -->
         <div class="list-nav">
            <ul>
               <li v-for="item in headerNavList" :key="item.url">
                  <a :href="item.url" :class="{ active: item.active }">{{ item.text }}</a>
               </li>
            </ul>
         </div>
      </nav>
   </header>
</template>

<script>
export default {
   name: "Header",
   props: ["headerNavList"],
   components: {},
   data() {
      return {};
   },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_vars.scss";
@import "../assets/sass/_mixins.scss";

header {
   height: 120px;

   .container {
      height: 100%;
      @include flex_ycenter_spaced();
   }
}
.list-nav {
   height: 100%;
}
ul {
   display: flex;
   text-transform: uppercase;
   height: 100%;

   li {
      list-style: none;
      margin-left: 1.2rem;

      a {
         text-decoration: none;
         color: black;
         font-weight: 600;
         height: 100%;
         @include flex_center("y");
         border-bottom: 3px solid #fff;

         &:hover {
            border-bottom: 3px solid $blue-dc;
         }
         &:active {
            border-bottom: 3px solid $blue-dc;
         }
      }

      .active {
         border-bottom: 3px solid $blue-dc;
      }
   }
}
</style>
