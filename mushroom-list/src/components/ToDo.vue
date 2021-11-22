<template>
 <div class="to-do-overall">
   <div class="box to-do-box">
     <h3 class="box-title">To-Do Box:</h3>
     <ul class="list">
       <li> 
         <input class="text-input"/>
       <input @click="finished" class="checkbox" type="checkbox">
       </li>
        <li> 
         <input class="text-input"/>
      <input @click="finished" class="checkbox" type="checkbox">
       </li> 
        <li> 
         <input class="text-input"/>
       <input @click="finished" class="checkbox" type="checkbox">
       </li>
        <li> 
         <input class="text-input"/>
       <input @click="finished" class="checkbox" type="checkbox">
       </li>
        <li> 
         <input class="text-input"/>
      <input @click="finished" class="checkbox" type="checkbox">
       </li>
     </ul>
   </div>
   <div class=" box finished-box">
     <h3 class="box-title">Finished Box:</h3>
   </div>
 </div>
</template>

<script>
export default {
  name: 'ToDo', 
  methods: {
    finished(){
      
    }
  }
}
</script>

<style scoped>
.to-do-overall{
  width: 100%;
  display: flex;
}
.box{
  width: 20rem;
  height: 13rem;
  border: white solid 0.1rem;
  border-radius: .3rem;
  margin-top: 3rem;
  background-color: #ffe3c6;
}
.to-do-box{
  margin-left: 4rem;
}
.finished-box{
  position: absolute;
  right: 4rem;
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
</style>
