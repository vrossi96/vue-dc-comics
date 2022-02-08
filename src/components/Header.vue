<template>
   <header>
      <nav class="container">
         <!-- Left part with logo -->
         <div><img src="../assets/img/dc-logo.png" alt="DC Logo" /></div>
         <!-- Right part with list -->
         <div>
            <ul>
               <li v-for="item in navList" :key="item.url">
                  <a :href="item.url">{{ item.text }}</a>
               </li>
            </ul>
         </div>
      </nav>
   </header>
</template>

<script>
export default {
   name: "Header",
   components: {},
   data() {
      return {
         navList: [
            { text: "characters", url: "#" },
            { text: "comics", url: "#" },
            { text: "movies", url: "#" },
            { text: "tv", url: "#" },
            { text: "games", url: "#" },
            { text: "collectibles", url: "#" },
            { text: "videos", url: "#" },
            { text: "fans", url: "#" },
            { text: "news", url: "#" },
            { text: "shop", url: "#" },
         ],
      };
   },
};
</script>

<style scoped lang="scss">
header {
   height: 120px;

   nav {
      height: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
   }
}
ul {
   display: flex;
   text-transform: uppercase;
}
li {
   list-style: none;
   margin-left: 1.2rem;

   a {
      text-decoration: none;
      color: black;
      font-weight: 600;
   }
}
</style>
