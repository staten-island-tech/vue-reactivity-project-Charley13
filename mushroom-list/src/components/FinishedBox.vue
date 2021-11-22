<template>
   <div class="box finished-box">
     <h3 class="box-title">Finished Box:</h3>
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
     </ul>
   </div>
</template>

<script>
export default {
name: "FinishedBox",
mounted(){
    this.$root.$on("listItem", (content) => {
        const populated = document.querySelectorAll(".populate li");
        populated.value = content;
        console.log(populated.value)
    }
    );
}
}
</script>

<style>

</style>