<template>
  <v-card height="500px">
    <plotlyChart :chartProperties = "chartProperties"></plotlyChart>
  </v-card>
</template>

<script>
import plotlyChart from "../components/plotlyChart";

export default {
  components: {
    plotlyChart
  },
  data() {
    return {
      chartProperties: {
        traces: [
          {
            x: [1, 2, 3, 4],
            y: [10, 15, 13, 17],
            mode: 'lines',
            name: "Vehicles",
            // marker: {
            //   size: 40,
            //   color: ["#fcba03", "#f5501d", "#bf7eb5", "#2bba8a"],
            //   symbol: ["diamond-open", "square", 'triangle-ne-dot', "x"],
            //   line: {
            //     color: ['rgb(0,0,0)', "#b88474", "#2aacf7" , "#59183e"],
            //     width: 6
            //   }
            // }
          },
          {
            x: [1, 2, 3, 4],
            y: [16, 5, 11, 9],
            mode: 'lines',
            name: "People",
            line: {
              color: ["#f5501d"],
              width: 3
            }
          },
          {
            x: [1, 2, 3, 4],
            y: [12, 4, 13, 3],
            mode: 'lines+markers',
            name: "Animals",
            // line: {
            //   dash: 'dashdot',
            //   color: ["#f5501d"],
            //   width: 10
            // },
            // marker: {
            //   size: 40,
            //   color: ["#fcba03", "#f5501d", "#bf7eb5", "#2bba8a"],
            //   symbol: ["diamond-open", "square", 'triangle-ne-dot', "x"],
            //   line: {
            //     color: ['rgb(0,0,0)', "#b88474", "#2aacf7", "#59183e"],
            //     width: 6
            //   }
            // }
          }
        ],
        layout: {
          title: {
            text:'Plot Title',
            font: {
              family: 'Courier New, monospace',
              size: 24
            },
            xref: 'paper',
            x: 0.05,
          },
          xaxis: {
            title: {
              text: 'x Axis',
              font: {
                family: 'Courier New, monospace',
                size: 18,
                color: '#7f7f7f'
              }
            },
          },
          yaxis: {
            title: {
              text: 'y Axis',
              font: {
                family: 'Courier New, monospace',
                size: 18,
                color: '#7f7f7f'
              }
            }
          },
          showlegend: true,
          legend: {
            bgcolor: "#dbd3d8",
            orientation: 'h',
            x:0.4,
            y:-0.3
          }
        }
      }
    }
  }
}
</script>
