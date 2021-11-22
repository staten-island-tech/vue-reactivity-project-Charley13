<template>
 <div class="app-overall">
<!-- Picture link: https://www.wallpaperflare.com/white-clouds-and-green-grass-field-wallpaper-pixel-art-pixels-digital-art-horizon-wallpaper-243952-->
   <div class="heading-box">
   <h1 class="heading app-title">Mushroom List</h1>
   <h2 class="heading app-subtitle">Complete tasks to add mushrooms + create a beautiful garden!</h2>
   </div>
   <ToDo />
<iframe class="video" width="150" height="100" src="https://www.youtube.com/embed/tBDVLey1DIE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen ></iframe>
 </div>
</template>

<script>
import ToDo from './components/ToDo.vue'

export default {
  name: 'App',
  components: {
     ToDo
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Amatic+SC:wght@700&family=Indie+Flower&display=swap');

html,body{
  margin: 0;
}
.app-overall{
  width: 100vw;
   height: 100vh;  
  background-image: url(./assets/background.jpg);
  background-size: contain;
}
.heading-box{
  width: 100%;
  display: flex;
flex-direction: column;
 justify-content: center;
 align-items: center;
 padding-top: 2.3rem;
}
.heading{
  margin: 0;
  color: white;
}
.app-title{
  font-family: 'Amatic SC', cursive;
  font-size: 4.5rem;
}
.app-subtitle{
  font-family: 'Indie Flower', cursive;
  font-size: 1.5rem;
}
.video{
 position: absolute;
 right: 1rem;
 top: 1rem;
}
</style>
