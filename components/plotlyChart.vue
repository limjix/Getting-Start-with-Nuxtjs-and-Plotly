<template>
  <div class="chart" :ref="chartID"></div>
</template>

<script>
import Plotly from 'plotly.js-dist'
import { v4 as uuidv4 } from 'uuid';
export default {
  name: "plotlyChart",
  props: {
    chartProperties: {
      type: Object,
      required: true
    }
  },
  components: {
    Plotly
  },
  data() {
    return {
      chartID: uuidv4()
    }
  },
  // watch: {
  //   chart: {
  //     handler: function() {
  //       this.chart.layout.datarevision = new Date().getTime();
  //       Plotly.react(
  //         this.$refs[this.chartID],
  //         this.chart.traces,
  //         this.chart.layout,
  //       );
  //     },
  //     deep: true
  //   }
  // },
  // computed: {
  //
  // },
  mounted() {
    Plotly.newPlot(this.$refs[this.chartID], this.chartProperties.traces, this.chartProperties.layout, {
      responsive:true,
      editable: true,
    });
  },
}
</script>

<style scoped>
.chart {
  height:100%;
  width:100%;
  padding-top: 5px;
}
</style>
