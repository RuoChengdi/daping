 <template>
  <div id="dataView">
    <dv-full-screen-container>
      <div class="mainHeader">
        <dv-border-box-11 title="CSDN数据分析"> </dv-border-box-11>
      </div>

      <dv-border-box-1 class="mainContainer">
        <dv-border-box-3 class="leftChartContainer">
          <LeftChartVue />
        </dv-border-box-3>

        <div class="rightMainContainer">
          <div class="rmcTopContainer">
            <dv-border-box-3 class="rmctc-left-container">
              <Map />
            </dv-border-box-3>

            <div class="rmctc-right-container">
              <dv-border-box-3 class="rmctc-chart-1">
                <dv-decoration-12 style="width: 150px; height: 150px" />
              </dv-border-box-3>

              <dv-border-box-4 class="rmctc-chart-2" :reverse="true">
                 <ActiveChartVue />
              </dv-border-box-4>
            </div>
          </div>

          <dv-border-box-4 class="rmcBottomContainer">
            <ScrollBoardVue />
          </dv-border-box-4>
        </div>
      </dv-border-box-1>
    </dv-full-screen-container>
  </div>
</template>
<script>
import dataList from "../assets/data/data.json";
import LeftChartVue from "../components/LeftChart.vue";
import ScrollBoardVue from "../components/ScrollBoard.vue";
import Map from "../components/Map.vue";
import ActiveChartVue from '../components/activeChart.vue';
export default {
  data() {
    return {
      dataList,
    };
  },
  components: {
    LeftChartVue,
    Map,
    ScrollBoardVue,
    ActiveChartVue
  },
};
</script>
<style lang="scss" scoped>
.rmctc-chart-1 ::v-deep .border-box-content{
   display: flex;
   justify-content: center;
   align-items: center;
}

.rmctc-chart-2 ::v-deep .border-box-content{
   display: flex;
   justify-content: center;
   align-items: center;
}
::v-deep #dv-full-screen-container {
  height: 100%;
}
#dataView {
  width: 100%;
  height: 100%;
  background-color: #030409;
  color: #fff;

  #dv-full-screen-container {
    background-image: url("../assets/bg.png");
    background-size: 100% 100%;
    box-shadow: 0 0 3px blue;
    display: flex;
    flex-direction: column;
  }

  .mainHeader {
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;

    .mh-left {
      font-size: 20px;
      color: rgb(1, 134, 187);

      a:visited {
        color: rgb(1, 134, 187);
      }
    }

    .mh-middle {
      font-size: 30px;
    }

    .mh-left,
    .mh-right {
      width: 450px;
    }
  }

  .mainContainer {
    height: calc(100% - 200px);
    // display: flex;
    ::v-deep .border-box-content {
      padding: 20px;
      box-sizing: border-box;
      display: flex !important;
    }
  }

  .leftChartContainer {
    width: 22%;
    padding: 10px;
    box-sizing: border-box;

    ::v-deep .border-box-content {
      flex-direction: column;
      display: flex;
    }
  }

  .rightMainContainer {
    width: 78%;
    padding-left: 5px;
    box-sizing: border-box;
  }

  .rmcTopContainer {
    height: 65%;
    display: flex;
  }

  .rmctc-left-container {
    width: 65%;
  }

  .rmctc-right-container {
    width: 35%;
  }

  .rmcBottomContainer {
    height: 35%;
  }

  .rmctc-chart-1,
  .rmctc-chart-2 {
    height: 50%;
  }
}

</style>