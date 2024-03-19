<template>
  <div class="col-lg-8 col-md-8 col-sm-12 col-xs-12">
    <q-card class="no-shadow" bordered>
      <q-card-section class="text-h6">
        Line Chart
      </q-card-section>
      <q-card-section>
        <ECharts :option="options"
                 class="q-mt-md"
                 :resizable="true"
                 autoresize style="height: 300px;"
        />
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import * as echarts from 'echarts'
import ECharts from "vue-echarts";
import {defineComponent} from "vue";
export default defineComponent({
  name: "LineChart",
  components:{
    ECharts
  },
  data() {
    return {
      options: {
        color: ['#80FFA5'],
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            type: 'cross',
            label: {
              backgroundColor: '#6a7985'
            }
          }
        },
        legend: {
          data: ['Line 1'],
          bottom: 10,
        },
        grid: {
          left: '3%',
          right: '4%',
          bottom: '20%',
          top: '5%',
          containLabel: true
        },
        xAxis: [
          {
            type: 'category',
            boundaryGap: false,
            data: ['10 Nov','15 Nov','25 Nov','30 Nov']
          }
        ],
        yAxis: [
          {
            type: 'value'
          }
        ],
        series: [
          {
            name: 'Line 1',
            type: 'line',
            stack: 'Total',
            smooth: true,
            lineStyle: {
              width: 0
            },
            showSymbol: false,
            areaStyle: {
              opacity: 0.8,
              color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                offset: 0,
                color: 'rgba(128, 255, 165)'
              }, {
                offset: 1,
                color: 'rgba(1, 191, 236)'
              }])
            },
            emphasis: {
              focus: 'series'
            },
            data: [140, 232, 101, 264, 90, 340, 250]
          }
        ]
      }
    }
  }
})
</script>

<style scoped>
</style>
