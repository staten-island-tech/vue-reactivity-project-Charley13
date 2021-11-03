<template>
  <div class="shelves">
    <!-- <ul>
      <li class="help" v-for="object in objects" :key="object.image">{{object.image}}</li>
    </ul> -->
    <div v-for="object in objects" :key="object.image" >
          <img class="images" :src="object.image" @click="moreInformation"/>
          <div class="info-box" v-show="isClicked">
            <div class="info-inner" >
            <h2 class="name">{{object.name}}</h2>
            <p class="description">{{object.information}}</p>
            <div class="button-div">
            <button class="add">Add Item</button>
            </div>
            </div>
          </div>
    </div>
  </div>
</template>

<script>
import key from "../assets/skeletonKey.svg"
import planets from "../assets/planets.svg"
import pumpkin from "../assets/pumpkin.svg"
import witch from "../assets/witch.svg"
export default {
  name: 'Shelves',
  props: {
  
  },
  data(){
    return{
      isClicked: false,
      objects: [
        {
          name: "Key",
          image: key,
          information: "RANDOM NONSENSE FOR NOW FOR TESTING",
        },
        {
          name: "Pumpkin",
          image: pumpkin,
          information: "Alright so it wasn't a good idea to keyboard smash in here for testing purposes.",
        },
         {
          name: "Planets",
          image: planets,
          information: "I want chocolateee.",
        },
        {
          name: "Witch hat",
          image: witch,
          information: "YTJYJYTJ",
        },
      ]
    }
  },
  methods: {
    moreInformation(){
//information overlay over object
this.isClicked = true;
    }
    //some functionality to add object to "cart", but you have to upload something in exchange
    //you're able to look at cart on a different page ... maybe a small button/icon appears in bottom right when you do the exchange
  }
}
</script>

<style scoped>
.shelves{
        margin: 0 auto;
         display: flex;
        justify-content: space-around;
        align-items: center; 
        position: relative; 
        height: 20rem;
        width: 100%;
}
.images{
  height: 100%;
  width: 12rem;
  position: absolute;
  top: 0;
  /* margin: 5rem 4rem 0 4rem; */
}
.info-box{
  height: 17rem;
  width: 12rem;
  top: 0;
  margin-top: 2rem;
    background-color: red; 
    border-radius: 0.4rem; 
  position: absolute;
  display: flex;
}
.info-inner{
  height: 80%;
  width: 80%;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-content: center;
  background-color: blue;
   border-radius: 0.4rem; 
}
.button-div{
  display: flex;
  justify-content: end;
}
.name{
  font-size: 1.5rem;
  background-color: aliceblue;
  margin-bottom: 1rem;
  margin-top: 0.5rem;
  text-align: center;
}
.description{
  font-size: 1rem;
  height: 7.5rem;
  background-color: pink;
    margin: 0;
    margin-bottom: 1rem;
}
.add{
  margin-right: 0.5rem;
}
</style>
