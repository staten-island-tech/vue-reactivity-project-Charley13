<template>
  <div class="shelves">
    <!-- <ul>
      <li class="help" v-for="object in objects" :key="object.image">{{object.image}}</li>
    </ul> -->
    <div v-for="object in objects" :key="object.image">
          <img class="help" :src="object.image" @click="moreInformation"/>
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
      objects: [
        {
          name: "Key",
          image: key,
        },
        {
          name: "Pumpkin",
          image: pumpkin,
        },
         {
          name: "Planets",
          image: planets,
        },
        {
          name: "Witch hat",
          image: witch,
        },
      ]
    }
  },
  methods: {
    moreInformation(){
   //uhhhhh run a series of text? In box? Based on the object you clicked?
    }
  }
}
</script>

<style scoped>
.shelves{
    height: auto;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
}
.help{
  height: 10rem;
  margin: 5rem 4rem;
}
</style>
