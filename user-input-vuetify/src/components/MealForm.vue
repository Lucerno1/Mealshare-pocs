<template>
    <v-row align="center" justify="center" >
        <v-col cols="10">

            <h1>Share a meal</h1>
            <!-- Text input fields -->
            <v-text-field color="green" class="mt-10" label="Title" outlined v-model="title"></v-text-field>
            
            <v-row>
                <v-col>
                    <v-text-field color="green"  label="Price" outlined v-model="price"></v-text-field>
                </v-col>
                <v-col>
                    <!-- Pop up dialog for timespan -->
                    <v-dialog max-width="308px" v-model="dialog">
                        <template v-slot:activator="{ on }">
                            <v-btn height="56px" color="grey" outlined x-large v-on="on">Set Pickup Time</v-btn>
                        </template>

                        <v-card >
                            <v-card-title class="headline grey lighten-2" primary-title>Set pickup time </v-card-title>
                            <v-card-actions class="d-flex flex-column">
                                <v-time-picker format="24hr" :allowed-minutes="(m) => m % 15 == 0" v-model="time"></v-time-picker>
                                <!-- Close the pop up dialog btn -->
                                <v-btn width="100%" class="mt-3" color="primary" depressed x-large  @click="dialog = false">Apply</v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-dialog>
                </v-col>
            </v-row>
            
                       
            

            <!-- Save to console log btn -->
            <v-row justify="center">
                <v-btn width="100%" class="white--text ma-3" large depressed elevation="0" color="green" v-on:click="myFunction">Save to console</v-btn>
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
            dialog: false,
            time: ""
        }
    },
    methods: {
        myFunction:function(){
            console.log({title:this.title, price:this.price, pickuptime:this.time})
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