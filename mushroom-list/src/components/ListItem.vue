<template>
      <li id="list-item"> 
         <input class="text-input"/>
       <input @click="addFinished" class="checkbox" type="checkbox">
       </li> 
</template>

<script>
export default {
name: "ListItem",
methods: {
    finished(){
       const trying = document.getElementsByTagName("li");
       const tryingArray = Array.from(trying);
       tryingArray.forEach(element => {
           const inputText = element.firstChild.value;
          this.$root.$emit("listItem", inputText)
       });
    },
     addFinished(){
          this.$root.$emit("counterNumber", counterNumber)
     }
}
}
</script>

<style>

</style>