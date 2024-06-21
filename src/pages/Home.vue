<template>
    <div>
      <h1>✦Check Weather Now✦</h1>
      <WeatherWidget />
    </div>
  </template>
  
  <script>
  import WeatherWidget from '../components/WeatherWidget.vue';
  
  export default {
    components: {
      WeatherWidget
    }
  };
  </script>
  
  <style scoped>
  h1{
    text-align: center;
  }
  </style>
  