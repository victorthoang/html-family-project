<template>
  <div class="about">
    
    <header id="top">
		<!--<h1 class="pageheader">About Me! (Contents)</h1>-->
		<!-- <hr> -->
		<!--<ul>
			<li class="linav">
				<a class="active" href="./index.html"><i class="fas fa-home fa-lg"></i> Home</a>
			</li>
			<li class="linav">
				<a href="#personal-statement">Personal Statement</a>
			</li>
			<li class="linav">
				<a href="#about-myself">About Myself</a>
			</li>
			<li class="linav">
				<a href="#hobbies" target="_blank">Hobbies</a>
			</li>
		</ul>-->
	</header>

  <main>
	<!-- <hr> -->
		<section id="about-me">
			<article id="personal-statement">
				<h3>Hello!</h3>
				<p>My name is Victor Hoang. I'm taking this Front End Web Development Certificate so that I can better understand the fundamentals of html, css, and javascript! I'm hoping that this will enable me to do 2 things:</p>
				<ol>
					<li>Create a front end web page from the ground up</li>
					<li>Understand the fundamentals of proper html practices and understand its possibilities and limitations.</li>
				</ol>
			</article>
			<article id="about-myself">
				<h2><a href="#about-myself">About Myself</a></h2>
				<img alt="Victor Hoang" src="../assets/Hoang-Victor.jpg" style="max-width:50%;height:auto">
				<ol>
					<li class="none">Birthday: Winter</li>
					<li class="none">Born and raised: Seattle, Washington.</li>
					<li>Washington State University</li>
					<li>University of washington (masters)</li>
					<li>Boeing's web browser(s) product manager</li>
				</ol>
			</article>
			<article id="hobbies">
				<h2><a href="#hobbies">Hobbies</a></h2>
				<p>None</p>
			</article>
			<h2>Questions?</h2>
			<div class="formbackground">
				<form>
				  <label for="fname">First Name</label>
				  <input type="text" id="fname" name="firstname" placeholder="Your name..">
			  
				  <label for="lname">Last Name</label>
				  <input type="text" id="lname" name="lastname" placeholder="Your last name..">
			  
				  <label for="inquiry-type">Inquiry Type</label>
				  <select id="inquiry" name="inquiry">
					<option value="general">general</option>
					<option value="social">social</option>
					<option value="professional">professional</option>
				  </select>

				  <label for="your-inquiry">Your Inquiry</label>
					<textarea name="your-inquiry" placeholder="Your comments here"></textarea>
					
				
				  <input type="submit" value="Submit">
				</form>
			  </div>




			<p><a href="#top">Return to top</a></p>
		</section>
		<aside>
			<a href="#top">More content coming soon! (place holder for aside tag)</a>
		</aside>
	</main>
  </div>
</template>

<style lang="scss">
li{
	list-style-type: none;
}
</style>