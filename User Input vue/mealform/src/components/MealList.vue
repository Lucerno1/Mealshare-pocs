<template>
    <div>
        <div v-bind:key="meal.id" v-for="meal in meals">
            <MealItem v-bind:meal="meal" />
        </div>
    </div>
</template>

<script>
import MealItem from './MealItem.vue';
export default {
    name: "MealList",
    components: {
        MealItem
    },
    props: ["meals"]
}
</script>

<style scoped>

</style>