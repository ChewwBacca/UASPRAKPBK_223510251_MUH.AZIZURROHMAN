<template>
  <q-card>
    <q-card-section>
      <div class="text-h6">Weather in {{ location }}</div>
      <q-input v-model="location" @keyup.enter="fetchWeather" placeholder="Enter location" />
      <q-btn @click="fetchWeather" label="Check" class="q-my-md" />
      <div v-if="weather.main">
        <div class="text-subtitle1">{{ weather.weather[0].description }}</div>
        <div>{{ Math.round(weather.main.temp - 273.15) }}°C</div>
      </div>
    </q-card-section>
    <q-separator />
    <q-card-actions align="right">
      <q-btn flat @click="fetchWeather">Refresh</q-btn>
    </q-card-actions>
  </q-card>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      weather: {},
      location: 'Pekanbaru'
    };
  },
  mounted() {
    this.fetchWeather();
  },
  methods: {
    fetchWeather() {
      const apiKey = 'b8d18946478140112e4ffa07e8b5f934';
      const apiUrl = `https://api.openweathermap.org/data/2.5/weather?q=${this.location}&appid=${apiKey}`;
      axios.get(apiUrl).then(response => {
        this.weather = response.data;
      }).catch(error => {
        this.$q.notify({
          color: 'negative',
          position: 'top',
          message: 'Location not found!',
          icon: 'warning'
        });
      });
    }
  }
};
</script>

<style scoped>
.q-card {
  max-width: 400px;
  margin: auto;
  padding: 20px;
}
</style>
