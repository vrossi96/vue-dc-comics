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
   props: ["topFooterList"],
   data() {
      return {};
   },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_mixins.scss";

#top-footer {
   color: #fff;
   height: 430px;
   background: url(../assets/img/footer-bg.jpg);
   @include bg_cov_norep_cent();

   .container {
      @include flex_ycenter_spaced();
   }

   .logo {
      height: 100%;
      background: url(../assets/img/dc-logo-bg.png);
      background-repeat: no-repeat;
      background-position: center;
   }
}
.list-container {
   width: 40%;
   max-height: 80%;
   display: flex;
   flex-direction: column;
   flex-wrap: wrap;
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
</style>
