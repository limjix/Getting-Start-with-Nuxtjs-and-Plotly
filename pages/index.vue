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

      }
    }
  }
}
</script>
