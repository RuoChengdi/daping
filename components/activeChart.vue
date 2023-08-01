<template>
  <div>
    <dv-decoration-9 style="width:180px;height:180px;">
        <p @click="handleGo">源码地址访问</p>
    </dv-decoration-9>
  </div>
</template>
 <<script>
 export default {
    methods: {
        handleGo(){
             window.loaction.href = ""
        }
    },
 }
 </script>