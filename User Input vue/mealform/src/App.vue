<template>
  <div id="app">
    <MealList v-bind:meals="meals" />
  </div>
</template>


<script>
import MealList from './components/MealList';



export default {
  name: 'App',
  components: {
    MealList
    
  },
  data(){
    return{
      meals: [
        {
          id:1,
          title: "Spaghetti",
          price: 3
        },
        {
          id:2,
          title: "Meatballs",
          price: 4
        },
        {
          id:3,
          title: "Pancakes",
          price: 2
        },
      ]
    }
  }
}
</script>


<style>
* {
  box-sizing:border-box;
  margin: 0;
  padding: 0;
}
</style>
