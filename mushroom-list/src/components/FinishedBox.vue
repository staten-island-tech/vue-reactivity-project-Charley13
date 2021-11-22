<template>
   <div class="box finished-box">
     <!-- <h3 class="box-title">Finished Box:</h3>
     <ul class="list populate">
          <li>
             <input class="text-input"/>
         </li>
         <li>
             <input class="text-input"/>
         </li>
         <li>
             <input class="text-input"/>
         </li>
         <li>
             <input class="text-input"/>
         </li>
         <li>
             <input class="text-input"/>
         </li> 
     </ul> -->
     <!-- <h4 class="box-title finished-title">Tasks Completed: {{counter}}</h4> -->
   </div>
</template>

<script>
export default {
name: "FinishedBox",
// data() {
//     return{
//         counter: 0,
//     } 
// },
// mounted(){
//     this.$root.$on("listItem", (content) => {
//         const populated = document.querySelectorAll(".populate li");
//         populated.value = content;
//         console.log(populated.value)
//     }, 
//     this.$root.$on("counterNumber", counter=+1)
//     );
// }
}
</script>

<style>
.finished-box{
    height: 7rem;
}
.finished-title{
    font-size: 3rem;
}
</style>