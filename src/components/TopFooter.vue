<template>
   <div id="top-footer">
      <div class="container">
         <div class="list-container">
            <div v-for="(list, index) in topFooterList" :key="index" class="footer-list">
               <h3>{{ list.text }}</h3>
               <ul>
                  <li v-for="item in list.list" :key="item.url">
                     <a :href="item.url">{{ item.text }}</a>
                  </li>
               </ul>
            </div>
         </div>
         <div class="w-50 logo"></div>
      </div>
   </div>
</template>

<script>
export default {
   name: "TopFooter",
   data() {
      return {
         topFooterList: [
            {
               text: "dc comics",
               list: [
                  { text: "Characters", url: "#" },
                  { text: "Comics", url: "#" },
                  { text: "Movies", url: "#" },
                  { text: "TV", url: "#" },
                  { text: "Games", url: "#" },
                  { text: "Videos", url: "#" },
                  { text: "News", url: "#" },
               ],
            },
            {
               text: "shop",
               list: [
                  { text: "Shop DC", url: "#" },
                  { text: "Shop DC Collectibles", url: "#" },
               ],
            },
            {
               text: "dc",
               list: [
                  { text: "Terms Of Use", url: "#" },
                  { text: "Privacy policy(New)", url: "#" },
                  { text: "Ad Choice", url: "#" },
                  { text: "Advertising", url: "#" },
                  { text: "Jobs", url: "#" },
                  { text: "Subscription", url: "#" },
                  { text: "CPSC Certificates", url: "#" },
                  { text: "Ratings", url: "#" },
                  { text: "Shop Help", url: "#" },
                  { text: "Contact Us", url: "#" },
               ],
            },
            {
               text: "sites",
               list: [
                  { text: "DC", url: "#" },
                  { text: "MAD Magazine", url: "#" },
                  { text: "DC Kids", url: "#" },
                  { text: "DC Universe", url: "#" },
                  { text: "DC Power Visa", url: "#" },
               ],
            },
         ],
      };
   },
};
</script>

<style scoped lang="scss">
#top-footer {
   color: #fff;
   height: 100vh;
   max-height: calc(100vh - 500px);
   background: url(../assets/img/footer-bg.jpg);
   background-size: cover;
   background-repeat: no-repeat;
   background-position: center;

   .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
   }

   .logo {
      height: 100%;
      background: url(../assets/img/dc-logo-bg.png);
      background-repeat: no-repeat;
      background-position: center;
   }
}
.footer-list {
   padding: 0 15px 15px 0;
}
h3 {
   text-transform: uppercase;
   padding-bottom: 15px;
}

li {
   list-style: none;

   a {
      text-decoration: none;
      color: rgb(141, 141, 141);
      font-weight: 300;
   }
}
.list-container {
   max-height: 80%;
   display: flex;
   flex-direction: column;
   flex-wrap: wrap;
}
</style>
