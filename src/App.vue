<template>
  <div>
    <div class="container">
      <button @click="componentToRender='comphome'">Home</button>
      <button @click="componentToRender='compcontact'">Contact</button>
      <button @click="componentToRender='compabout'">About</button>
        <keep-alive>

             <component :is="componentToRender"></component>

        </keep-alive>
        
      
    </div>
  </div>
</template>

<script>
import comphome from './Components/home';
import compabout from './Components/about';
import compcontact from './Components/contact';
export default {
    data(){
      return{
         componentToRender: 'compcontact'
      }
    },
    components:{
      comphome,
      compabout,
      compcontact
    }
}
</script>

<style>
   button{
     padding-left: 5px;
   }

</style>