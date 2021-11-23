<template>
 <div class="to-do-overall">
   <div class="box to-do-box">
     <h3 class="box-title">To-Do Box:</h3>
     <ul class="list">
     <li id="list-item"> 
         <input class="text-input" />
       <input @click="addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input" />
       <input @click=" addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input" />
       <input @click="addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input" />
       <input @click="addMushroom" class="checkbox" type="checkbox">
       </li> 
       <li id="list-item"> 
         <input class="text-input" />
       <input @click="addMushroom" class="checkbox" type="checkbox">
       </li> 
     </ul>
   </div>
  <div class="box finished-box">
     <h4 class="box-title finished-title">Tasks Completed: {{counter}}</h4>
     <ul class="list-two" v-for="val in newVals" :key="val">
       <li class="text-input-two" ></li>
     </ul>
   </div>
   <div class="mushroom-overall">
   <div class="mushroom-box" v-for="musrhoom in musrhooms" :key="musrhoom">
      <!-- add mushroom picture to array to generate mushrooms, el can just be 2, 2 items => 2 mushrooms -->
     <img src="../assets/mushroom.png" class="mushroom-img">
   </div>
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
      musrhooms: [],
      newVals: [],
    }
  }, 
  methods: {
     addMushroom(){
       this.counter++;
       this.musrhooms.push(this.counter);
      //  const ogLi = document.getElementsByTagName("li");
      //  const ogLiArray = Array.from(ogLi);
      //  ogLiArray.forEach(element => {
         
      //   const value = element.firstChild.value;
      //    this.newVals.push(value);
      //           console.log(value);
         
      //  });
     }
  }
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
.list, .list-two{
    margin: 0;
  padding: 0;
  margin-left: 2rem;
}
.text-input, .text-input-two{
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
.mushroom-overall{
  display: flex;
  flex-direction: row;
  position: absolute;
width: 100%;
justify-content: center;
bottom: 9rem;
}
.mushroom-box{
/* margin: auto; */
/* position: absolute;
bottom: 0;
width: 100%; */
display: flex;
justify-content: space-between;
}
.mushroom-img{
  width: 4rem;
  height: 6rem;
  margin-left: 2rem;
}
</style>
