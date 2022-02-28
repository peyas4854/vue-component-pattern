<template>
  <div>
    <div v-for="(user,i) in users" :key="i">
      <WeatherCard
          :username="user.name"
          :companyName="user.company.name "
          :email="user.email"
          :websiteLink="user.website"
      ></WeatherCard>
    </div>
  </div>
</template>
<script>
import WeatherCard from "../components/WeatherCard.vue";
import axios from "axios";
// import axios from "axios";
export default {
  data() {
    return {
      users: [],
    }
  },
  components: {
    WeatherCard,
  },
  created() {
    this.getWeatherData();
  },
  methods: {
    getWeatherData() {
      axios.get('https://jsonplaceholder.typicode.com/users')
          .then(response => {
            console.log('sdf', response.data);
            this.users = response.data;
          })
    },
  },
};
</script>
