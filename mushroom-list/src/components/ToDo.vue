<template>
 <div class="to-do-overall">
   <div class="box to-do-box">
     <h3 class="box-title">To-Do Box:</h3>
     <ul class="list">
      <ListItem />
       <ListItem />
        <ListItem />
         <ListItem />
          <ListItem />
     </ul>
   </div>

 </div>
</template>

<script>
import ListItem from "./ListItem.vue"
export default {
  name: 'ToDo', 
  components: {
    ListItem,
  },

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
</style>
