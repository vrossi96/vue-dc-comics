<template>
   <header>
      <nav class="container">
         <!-- Left part with logo -->
         <div><img src="../assets/img/dc-logo.png" alt="DC Logo" /></div>
         <!-- Right part with list -->
         <div class="list-nav">
            <ul>
               <li v-for="item in navList" :key="item.url">
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
   components: {},
   data() {
      return {
         navList: [
            { text: "characters", url: "#", active: true },
            { text: "comics", url: "#", active: false },
            { text: "movies", url: "#", active: false },
            { text: "tv", url: "#", active: false },
            { text: "games", url: "#", active: false },
            { text: "collectibles", url: "#", active: false },
            { text: "videos", url: "#", active: false },
            { text: "fans", url: "#", active: false },
            { text: "news", url: "#", active: false },
            { text: "shop", url: "#", active: false },
         ],
      };
   },
};
</script>

<style scoped lang="scss">
header {
   height: 120px;

   .container {
      height: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
   }
}
.list-nav {
   height: 100%;
}
ul {
   display: flex;
   text-transform: uppercase;
   height: 100%;
}
li {
   list-style: none;
   margin-left: 1.2rem;

   a {
      text-decoration: none;
      color: black;
      font-weight: 600;
      height: 100%;
      display: flex;
      align-items: center;
      border-bottom: 3px solid #fff;

      &:hover {
         border-bottom: 3px solid #0282f9;
      }
      &:active {
         border-bottom: 3px solid #0282f9;
      }
   }
}
.active {
   border-bottom: 3px solid #0282f9;
}
</style>
