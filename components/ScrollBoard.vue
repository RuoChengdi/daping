<template>
     <div class="center">
        <dv-scroll-board :config="config" style="width:75vw;height:100%" />
     </div>
</template>
<script>
import dataList from '../assets/data/data.json'

export default {
    data() {
        return {
            dataList,
            config:{
                header: ['标题', '作者',"阅读数量", '发布时间'],
                data:[],
                sort:true,
                 align: ['center']
            }
        }
    },
    mounted() {
        this.dataList.forEach(item => {
            this.config.data.push(
                [item.title, item.author, item.read,item.pushTime]
            )
        });
    },
}
</script>
<style lang="scss" scoped>
::v-deep .rows{
     border-bottom-left-radius: 20px;
     border-bottom-right-radius: 20px;
}
::v-deep .dv-scroll-board .header{
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
}
</style>