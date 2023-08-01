<template>
  <div>
    <p class="myCoding" @click="handleGo">源码地址访问</p>
    <dv-decoration-9 style="width: 180px; height: 180px">
      <!-- <p @click="handleGo">源码地址访问</p> -->
      <!-- <dv-link to="https://pandengzheflag.coding.net/public/shujudaping/nuxtdaping/git/files"   >源码地址访问</dv-link> -->
    </dv-decoration-9>
  </div>
</template>
 <<script>
 export default {
  methods: {
      handleGo(){
           console.log(123);
           window.location.href = "https://pandengzheflag.coding.net/public/shujudaping/nuxtdaping/git/files"
        }
  },
   
 }
 </script>
 <style lang="scss" scoped>
 .myCoding{
  position: absolute;
  width: 180px;
  text-align: center;
  line-height: 180px;
  z-index: 100000;  
  cursor: pointer;
 }
 </style>