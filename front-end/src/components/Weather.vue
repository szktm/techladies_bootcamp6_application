<template>
    <div>
    <h1>What's the weather in Singapore?</h1>
    <h2>Area, Forecast</h2>
    <!-- The alignment of the unordered list is off-centre but idk how to fix -->
    <ul id="Weather" class="container" v-for="forecast in info" :key="forecast.value" >
    {{forecast.area}}, {{forecast.forecast}}
    </ul>
  </div>

</template>


<script>
import axios from 'axios'
export default {
  name: 'Weather',
  data(){
    return {
      info: null
    }
  },
  mounted() {
       axios
        .get('https://api.data.gov.sg/v1/environment/2-hour-weather-forecast')
        .then(response => (this.info = response.data.items[0].forecasts))
        
  }
}
</script>
