<template>
<h1>My Family Site</h1>
  <div class="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/Family">Family</router-link>
  </div>
  <router-view/>

  <footer class="pagefooter">
    <div class="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/Family">Family</router-link>
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
        </ul>
		<small>&#169;2020 Victor Hoang Inc. All rights reserved. | Seattle, WA</small>
	</footer>
</template>

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
</style>
