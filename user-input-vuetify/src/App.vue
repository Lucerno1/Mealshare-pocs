<template>
  <v-app>
    <MealForm />
  </v-app>
</template>

<script>
import MealForm from './components/MealForm';

export default {
  name: 'App',

  components: {
    MealForm,
  },

  data: () => ({
    //
  }),
};
</script>
