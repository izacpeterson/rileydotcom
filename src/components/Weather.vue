<script>
export default {
  data() {
    return {
      temp: 0,
      humi: 0,
    };
  },
  mounted() {
    //api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&appid=35701ad524635b065706933439a9ab30
    navigator.geolocation.getCurrentPosition(async (position) => {
      let lat = position.coords.latitude;
      let long = position.coords.longitude;

      console.log(position.coords);
      let url = "https://api.openweathermap.org/data/2.5/weather?lat=" + lat + "&lon=" + long + "&appid=35701ad524635b065706933439a9ab30&units=imperial";

      let rawData = await fetch(url);
      let jsonData = await rawData.json();
      console.log(jsonData.main.temp);
      this.temp = Math.round(jsonData.main.temp);
      this.humi = jsonData.main.humidity;
    });
  },
};
</script>
<template>
  <div>
    <ul>
      <h3>Temperature: {{ temp }}&deg;</h3>
      <h3>Humidity: {{ humi }}%</h3>
    </ul>
  </div>
</template>
<style></style>
