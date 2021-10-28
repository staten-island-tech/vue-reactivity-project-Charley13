<template>
  <div class="shelves">
    <!-- <ul>
      <li class="help" v-for="object in objects" :key="object.image">{{object.image}}</li>
    </ul> -->
    <div v-for="object in objects" :key="object.image">
          <img class="images" :src="object.image" @click="moreInformation"/>
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
          information: "RANDOM NONSENSE FOR NOW FOR TESTING",
        },
        {
          name: "Pumpkin",
          image: pumpkin,
          information: "THYTJFUYKIUOPP;FCHST546W45YGSFGHFGHFGH",
        },
         {
          name: "Planets",
          image: planets,
          information: "UTYIYUKGKDTFGHSERTSERTESRTERTESRTERTERRTTRTSTRSSRRSSSEHMNJHKYUK",
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
    }
    //some functionality to add object to "cart", but you have to upload something in exchange
    //you're able to look at cart on a different page ... maybe a small button/icon appears in bottom right when you do the exchange
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
.images{
  height: 10rem;
  margin: 5rem 4rem;
}
</style>
