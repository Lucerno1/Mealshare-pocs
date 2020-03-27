<template>
    <v-row align="center" justify="center" >
        <v-col cols="10">
            <v-text-field color="green" class="mx-10 mt-10" label="Title" outlined v-model="title"></v-text-field>
            <v-text-field color="green" class="mx-10" label="Price" outlined v-model="price"></v-text-field>
            <v-text-field color="green" class="my-input mx-10" label="Timespan" outlined v-model="timespan"></v-text-field>

            <!-- <input v-model="title" placeholder="Title"> 
            <input v-model="price" placeholder="Price">
            <input v-model="timespan" placeholder="Timespan"> -->

            <v-row justify="center">
                <v-btn class="white--text mx-10" depressed elevation="0" color="green" v-on:click="myFunction">Save to console</v-btn>
            </v-row>
        </v-col>
    </v-row>
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


<style>

/* Test round borders for text-field */

/* .my-input.v-input .v-input__slot {
  border-radius: 100px;
}

.v-application--is-ltr .v-text-field--outlined legend{
    margin-left: 50px;
}

.v-application--wrap.v-input.v-input__control.v-input__slot.v-text-field__slot.v-application--is-ltr .v-text-field--outlined legend{
    margin-left: 50px !important;
} */



</style>