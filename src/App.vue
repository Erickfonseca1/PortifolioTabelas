<template>
  <v-app>
    <v-main>
      <NutricionTable/>
    </v-main>
  </v-app>
</template>

<script>
import NutricionTable from './components/NutricionTable.vue';

export default {
  name: 'App',

  components: {
    NutricionTable,
  },

  data: () => ({
    //
  }),
};
</script>
