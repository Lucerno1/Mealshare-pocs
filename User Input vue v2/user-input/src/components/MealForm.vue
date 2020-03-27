<template>
    <div>
        <input v-model="title" placeholder="Title">
        <input v-model="price" placeholder="Price">
        <input v-model="timespan" placeholder="Timespan">
        
        <button v-on:click="myFunction">Save</button>
    </div>
</template>


<script>
export default {
    name: 'MealForm',
    data(){
        return{
            title: "",
            price: "",
            timespan: ""
        }
    },
    methods: {
        myFunction:function(){
            console.log({title:this.title, price:this.price, timespan:this.timespan})
        }
    }
}
</script>


<style scoped>

</style>