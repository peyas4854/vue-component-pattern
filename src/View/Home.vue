<template>
  <div>
    <WeatherCard></WeatherCard>
  </div>
</template>

<script>
import WeatherCard from "../components/WeatherCard.vue";
import axios from "axios";

export default {

  components: {
    WeatherCard,
  },
  created() {
    console.log('sf');
    this.getWeatherData();
  },
  methods: {
    getWeatherData() {
      console.log('ddd');
      axios.get('https://api.coindesk.com/v1/bpi/currentprice.json')
          .then(response => {
            console.log('sdf',response);
          })
    },
  },
};
</script>
