<template>
<main>
	<!-- <hr> -->

    <button @click="toggleShowBlog">
        <span v-if="showBlog">Hide blog 1</span>
        <!-- <span v-if="!showBlog">Show Blog</span> -->
        <span v-else>Show blog 1</span>
    </button>
<div v-if="showBlog">
		<section>
			<h2 id="main-content">Blog post 1</h2>
            <p>In our lesson 7 homework in May 2021, I learned how to use Vue for the first time. To display my family from Vue, I'm using a v-for and it is displaying my family in an array! Have a look!</p>
            <ul>
                <li class="liFamily" v-for="person in familyMembers" v-bind:class="{fav: person.isFav}">
                    <img v-bind:src="person.img" alt="person.name">
                    <h3>{{person.name}}</h3>
                    <p>birthday: {{person.birthday}}</p>
                </li>
            </ul>
            
		</section>
    </div>

    <button @click="toggleShowBlog2">
        <span v-if="showBlog2">Hide blog 2</span>
        <!-- <span v-if="!showBlog">Show Blog</span> -->
        <span v-else>Show blog 2</span>
    </button>
<div v-if="showBlog2">
        <section>
			<h2 id="main-content">Blog post 2</h2>
			<p>This is the second blog post in my page.</p>
			<i class="fas fa-home"></i>
			<p>In the mean time, here is a photo of my favorite doggo, Kaydee!</p>
			<img alt="cute golden retriever staring back at the camera innocently" src="images/kaydee.jpg" width=400px height=500px>
		</section>
    </div>
	</main>
</template>

<script>
export default {
  name: 'Blog',
data() {
        return {
        showBlog: true,
        showBlog2: true,
        familyMembers: [
            {name: 'Victor Hoang', birthday: '12/16/1990', img: './assets/file-icon.png', isFav: true}, 
            {name: 'George Hoang', birthday: '12/06/1988', img: './assets/George.PNG', isFav: false}, 
            {name: 'Daniel Hoang', birthday: '08/07/1995', img: 'images/file-icon.png', isFav: false}, 
            {name: 'Du Hoang', birthday: '12/25/1950', img: 'images/file-icon.png', isFav: true},
            {name: 'Nhi Truong', birthday: '11/14/1960', img: 'images/file-icon.png', isFav: false},
        ],
        counter: 0,
        name: "victor",
        greeting: this.generateGreeting(),
        favNumbers: [3, 6, 15],
        imageShowing: false,
        imgSrc: ["https://picsum.photos/200/300"]    
    }
    },
    methods:{
        plusOne(){
            this.counter += 1
        },
        addMore(amt){
            this.counter += parseInt(amt)
        },
        generateGreeting(){
            return "Hello there! "
        },
        toggleImage(){
            this.imageShowing = true
        },
        toggleShowBlog(){
            this.showBlog = !this.showBlog
        },
        toggleShowBlog2(){
            this.showBlog2 = !this.showBlog2
        },
        
        // randomItem (items) {
        //         return items[Math.floor(Math.random()*items.length)];
        //     },
        //     generate () {
        //         this.selectedImage = this.randomItem(this.images)
        //     }
        // },
        // created() {
        //     this.selectedImage = this.randomItem(this.images)
        

    }
}

</script>

<style>
.liFamily{
  list-style-type: none;
  background: #fff;
  margin: 2rem auto;
  padding: 1rem 2rem;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}
img {
  width: 100%;
  height: auto;
}

li.fav{
  background-color: #ff9ed2;
  color: white;
}
ul{
    display: flex;
  flex-direction: column;
  background-color: lightsteelblue;
}
</style>