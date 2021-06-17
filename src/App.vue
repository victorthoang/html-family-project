<template>
<h1>My Family Site</h1>
  <div class="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/Family">Family</router-link> |
    <router-link to="/Blog">Blog</router-link>
  </div>
  <router-view/>

  <footer class="pagefooter">
    <small>&#169;2021 Victor Hoang Inc. All rights reserved. | Seattle, WA</small>
    <!--<div class="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/Family">Family</router-link> |
  </div>

        <img src="images/adoptadog-logo.svg" alt="adoptadog-logo" width="400px">
        <p>Aborpos nisto inci tet aut que volupti beruptiberro to ex <br>
            esseque invenienihil imaximu scideru ptistiusam consequunt</p>
        <ul class="ulnavfooter">
			<li class="linavfooter">
                <a class="active" href="./index.html">Home</a>
			</li>
			<li class="linavfooter">
				<a href="./dogs.html">Dogs</a>
			</li>
			<li class="linavfooter">
				<a href="./contact.html">Contact</a>
            </li>
        </ul>-->
		
	</footer>
  <!--Starting your weather app-->
  <!--<div id="app">
    <main>
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
    </main>
  </div>-->
</template>

<script>
// export default{
//   name: 'app',
//   data () {
//     return {
//       api_key: '6a2fb9cd555dc989c6acf44214b21acf',
//       url_base: 'https://api.openweathermap.org/data/2.5/',
//       query: '',
//       weather: {}
//     }
//   },
//   methods: {
//     fetchWeather (e) {
//       if(e.key == "Enter"){
//         fetch(`${this.url_base}weather?q=${this.query}&units=imperial&APPID=${this.api_key}`)
//           .then(res => {
//             return res.json();
//           }).then(this.setResults);
//       }
//     },
//     setResults (results){
//       this.weather = results;
//     },
//     dateBuilder () {
//       let d = new Date();
//       let months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
//       let days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

//       let day = days[d.getDay()];
//       let date = d.getDate();
//       let month = months[d.getMonth()];
//       let year = d.getFullYear();

//       return `${day} ${date} ${month} ${year}`;
//     }
//   }
// }
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.nav {
  padding: 30px;
  background-color: #30E3CA;
  margin: 0, 0;

  a {
    font-weight: bold;
    color: #2c3e50;a

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

html{
  background-color: #11999E;
}

.pagefooter{
    background-color:#3a3a3a;
    text-align:center;
    color: #ffffff;
    /* background-image: url(../images/adoptadog-logo.svg); */
    background-size: cover;
    width: 100%;
    clear: both;
    padding: 40px 0 20px 0;
    background-color: #093c60;
}
p, h3, ul{
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

html{
    height: 100%;
}

.hidden{
  position: relative;
  left: -10000px;
  top: auto;
}
.hidden:focus{
  left: 0;
}

hr { 
    display: block;
    margin-top: 0.0em;
    margin-bottom: 0.0em;
    margin-left: -40px;
    margin-right: auto;
    border-style: inset;
    border-width: 2px;
  } 
.pageheader{
    background-color:#11999E;
    /* color: #E4F9F5; */
    color: white;
    margin: 0 0 0 0;
    padding: 20px 20px 20px 20px;
    font-weight: bold;
}
main{
    /* border: 1px solid black; */
    margin-top: 0px;
    margin-bottom: 0px;
    margin-right: 2rem;
    margin-left: 2rem;
    background-color: lightsteelblue;
    padding: 2rem;
}
.footer{
    background-color:#11999E;
    margin: 0 0 0 0;
    padding: 20px 20px 20px 20px;
    font-weight: bold;
    flex-shrink: 0;
    /* color: #E4F9F5; */
    color:white;
}
body{
    font-size: 16px;
    font-family:'Noto Sans', sans-serif;
    /* color: #E4F9F5; */
    margin: 0 0 0 0;
    background-color: #FCF6F5FF;
    /* background-color: #565A5C; */
    height: 100%;
    display: flex;
    flex-direction: column;
    background-color:#11999E;
}

.content{
  flex: 1 0 auto;
}

a:hover{
    background-color:burlywood;
    color:darkmagenta;
    transition: 500ms;
}
a:visited{
    color:midnightblue;
}
img{
    border-style:outset;
}
.imgLesson6:hover{
  transform: rotate(45deg);
  transition-duration:500ms;
  width: 10rem;
  height: 10rem;
}
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #30E3CA;
    position: sticky;
    top: 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  .linav {
    float: left;
  }
  
  .linav a {
    display: inline-block;
    transition: 500ms;
    color: #545454;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
  }
  .linav a:hover {
    background-color:darkgray;
    font-size: 1.25rem;
  }
  * {
    box-sizing: border-box;
  }

section article:nth-child(even){
    background-color: #e6e6e6;
    padding: 2rem;
}
section article:nth-child(odd){
    background-color: #f2f2f2;
    padding: 2rem;
}

main h3{
  background-color:seagreen;
  padding: 1rem;
}

input[type=text], select {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type=submit] {
  width: 100%;
  background-color: #4CAF50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #45a049;
}

.formbackground {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}

textarea {
  width: 100%;
  height: 150px;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  background-color: #f8f8f8;
  font-size: 16px;
  resize: none;
  margin: 8px 0;
}
</style>
