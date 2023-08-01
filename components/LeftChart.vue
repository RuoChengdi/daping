<template>
  <div class="leftChart">
    <div class="lc1Header">【腾讯云 Cloud Studio 实战训练营】</div>
    <div class="lcDetails"> 参赛文章数量<span>{{dataList.length}}</span></div>
    <dv-scroll-ranking-board  class="lc3-chart" :config="config" />
    <!-- <dv-decoration-2 style="height:10px;" /> -->
  </div>
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
        this.dataList.forEach(item => {
            // console.log(item)
            this.config.data.push({
                 name:item.author,
                 value:Number(item.read)
            })
        });
    },
}
</script>
<style lang="scss" scoped>
.leftChart {
  width: 100%;
  height: 100%;
  display: flex;
  flex-grow: 0;
  flex-direction: column;

  .lc1Header {
    text-align: center;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 14px;
    margin-bottom: 20px;
  }

  .lcDetails {
    height: 50px;
    font-size: 10px;
    display: flex;
    align-items: center;
    text-indent: 20px;

    span {
      color: #096dd9;
      font-weight: bold;
      font-size: 35px;
      margin-left: 20px;
    }
  }

  .lc1-chart {
    flex: 1;
  }
}
</style>