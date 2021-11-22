<template>
      <li id="list-item"> 
         <input class="text-input"/>
       <input @click="finished" class="checkbox" type="checkbox">
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
    }
}
}
</script>

<style>

</style>