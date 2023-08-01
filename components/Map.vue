<template>
    <div>
        <dv-decoration-11 style="width:200px;height:60px;">前八点赞数据</dv-decoration-11>
        <dv-conical-column-chart :config="config" style="width:700px;height:316px;" /></div>
</template>
<script>
import dataList from '../assets/data/data.json'

export default {
    data() {
        return {
             dataList,
            config:{
              data:[],
             sort:true
            }
        }
    },
      mounted() {
        let strDatalist =  this.dataList.slice(0,8)
        strDatalist.forEach(item => {
            // console.log(item)
            this.config.data.push({
                 name:item.author,
                 value:Number(item.zan)
            })
        });
    },
}
</script>
<style lang="scss" scoped>
::v-deep .dv-decoration-11{
     margin: 0 auto;
}
</style>