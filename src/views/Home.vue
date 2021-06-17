<template>
  <!--<div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>-->
<main>
	<!-- <hr> -->
	<section>
		<h2 id="main-content">Hello!</h2>
		<p>Welcome to the landing page of my Html 300 family project! I wanted to create this site to create a foundation for a tool that can help my relatives identify each other. Since our family is so big, sometimes it is difficult for us to know everyones name. With this website, no longer will there be awkward moments where we can't identify someone at a family party!</p>
		
	</section>

	<section>
	<h2>Check the Weather!</h2>
	<p>Type in a City, Country, or Zipcode to figure out if the weather is ideal for a family outing!</p>
		<div id="app">
		<div class="search-box">
		<input type="text"
		class="search-bar"
		placeholder="Search...(City, State, Zipcode)" 
		v-model="query"
		@keypress="fetchWeather"
		/>
		</div>
		<div class="weather-wrap" v-if="typeof weather.main != 'undefined'">
		<div class="location-box">
			<div class="location">Place: {{weather.name}}, {{weather.sys.country}}</div>
			<div class="date">Date: {{dateBuilder()}}</div>
		</div>

		<div class="weather-box">
			<div class="temp">Temperature: {{Math.round(weather.main.temp)}}°F</div>
			<div class="weather">Climate: {{weather.weather[0].main}}</div>
		</div>
		</div>
		</div>
	</section>
</main>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  methods:{

  },
	name: 'app',
  data () {
    return {
      api_key: '6a2fb9cd555dc989c6acf44214b21acf',
      url_base: 'https://api.openweathermap.org/data/2.5/',
      query: '',
      weather: {}
    }
  },
  methods: {
    fetchWeather (e) {
      if(e.key == "Enter"){
        fetch(`${this.url_base}weather?q=${this.query}&units=imperial&APPID=${this.api_key}`)
          .then(res => {
            return res.json();
          }).then(this.setResults);
      }
    },
    setResults (results){
      this.weather = results;
    },
    dateBuilder () {
      let d = new Date();
      let months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
      let days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

      let day = days[d.getDay()];
      let date = d.getDate();
      let month = months[d.getMonth()];
      let year = d.getFullYear();

      return `${day} ${date} ${month} ${year}`;
    }
  }
}
</script>

<style>
main{
  background-color: lightsteelblue;
}
</style>