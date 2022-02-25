<template>
  <div>
    <WeatherCard></WeatherCard>
  </div>
</template>

<script>
import WeatherCard from "../components/WeatherCard.vue";
export default {
  data() {
    return {
      wweather: [],
    };
  },
  components: {
    WeatherCard,
  },
  mounted(){
      this.getWeatherData();
  },
  methods: {
    getWeatherData() {
      fetch("http://https://jsonplaceholder.typicode.com/users")
        .then((response) => response.json())
        .then((data) => console.log(data));
    },
  },
};
</script>
