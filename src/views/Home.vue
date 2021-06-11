<template>
  <!--<div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>-->
<main>
	<!-- <hr> -->
		<section id="Assignments" >
			<h2 id="main-content">Hello!</h2>
			<p>Welcome to the landing page of my Html 110 Portfolio! Future content will be added here as soon as I come up with content.</p>
			<i class="fas fa-home"></i>
			<p>In the mean time, here is a photo of my favorite doggo, Kaydee!</p>
			<img alt="cute golden retriever staring back at the camera innocently" src="images/kaydee.jpg" width=400px height=500px>
		</section>
			<p>Or, if you prefer 
				<span class="sr-only">this link opens in a new tab</span>
				<a href="https://victorthoang.github.io/mockup/" target=_blank> cats</a>
				...then you're one of THOSE PEOPLE!</p>

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
}
</script>

<style>
main{
  background-color: lightsteelblue;
}
</style>