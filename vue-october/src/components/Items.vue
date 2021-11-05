<template>
  <div class="item">
<img class="images" @click="moreInformation"/>
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
</template>

<script>
import key from "../assets/skeletonKey.svg"
import planets from "../assets/planets.svg"
import pumpkin from "../assets/pumpkin.svg"
import witch from "../assets/witch.svg"
export default {
name: "Items",
  data(){
    return{
      isClicked: false,
      // objects: [
      //   {
      //     name: "Key",
      //     image: key,
      //     information: "RANDOM NONSENSE FOR NOW FOR TESTING",
      //   },
      //   {
      //     name: "Pumpkin",
      //     image: pumpkin,
      //     information: "Alright so it wasn't a good idea to keyboard smash in here for testing purposes.",
      //   },
      //    {
      //     name: "Planets",
      //     image: planets,
      //     information: "I want chocolateee.",
      //   },
      //   {
      //     name: "Witch hat",
      //     image: witch,
      //     information: "YTJYJYTJ",
      //   },
      // ]
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

<style>

</style>