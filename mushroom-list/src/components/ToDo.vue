<template>
 <div class="to-do-overall">
   <div class="box to-do-box">
     <h3 class="box-title">To-Do Box:</h3>
     <ul class="list">
     <li id="list-item"> 
         <input class="text-input"/>
       <input @click="counter+=1,addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input"/>
       <input @click="counter+=1, addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input"/>
       <input @click="counter+=1, addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input"/>
       <input @click="counter+=1, addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input"/>
       <input @click="counter+=1, addMushroom" class="checkbox" type="checkbox">
       </li> 
     </ul>
   </div>
  <div class="box finished-box">
     <h4 class="box-title finished-title">Tasks Completed: {{counter}}</h4>
   </div>
   <div class="mushroom-box">
     <img v-show="counter===1" src="../assets/mushroom.png" class="mushroom-img">
     <img v-show="counter===2" src="../assets/mushroom.png" class="mushroom-img">
     <img v-show="counter===3" src="../assets/mushroom.png" class="mushroom-img">
     <img v-show="counter===4" src="../assets/mushroom.png" class="mushroom-img">
     <img v-show="counter===5" src="../assets/mushroom.png" class="mushroom-img">
   </div>
 </div>
</template>

<script>
// import ListItem from "./ListItem.vue"

export default {
  name: 'ToDo', 
  components: {
    // ListItem,
  },
  data(){
    return{
      counter: 0, 
      counterNumber: false,
    }
  }, 
//   methods: {
// addMushroom(){
// if(counter = 1){
//   counterNumber = true;
// }
// }
//   }

}
</script>

<style >
.to-do-overall{
  width: 100%;
  display: flex;
}
.box-title{
  margin-top: 0.5rem;
  margin-left: 0.5rem;
  margin-bottom: 0.2rem;
  text-decoration: underline;
  font-family: 'Indie Flower', cursive;
}
.list{
    margin: 0;
  padding: 0;
  margin-left: 2rem;
}
.text-input{
  width: 80%;
  height: 10%;
  border: none;
  outline: none;
  border-bottom: solid 0.1rem black;
  margin-bottom: 0.5rem;
    background-color: #ffe3c6;
}
.checkbox{
  margin-left: 1rem;
  width: 1rem;
  height: 1rem;
}
.mushroom-box{
  position: absolute;
  bottom: 10rem;
  left: 30rem;
  height: 5rem;
  width: 30rem;
}
.mushroom-img{
  width: 4rem;
  height: 6rem;
  margin-right: 2rem;
}
</style>
