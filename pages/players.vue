<template>
  <v-data-table
    :headers="headers"
    :items="players"
    :items-per-page="5"
    class="elevation-1"
  >
    <template v-slot:item.rating="{ item }">
      <v-rating :value="item.rating"></v-rating>
    </template>
  </v-data-table>
</template>

<script lang="js">
export default {
  name: "players.vue",
  data() {
    return {
      headers: [
        {text: 'Name', value: 'name',},
        {text: 'Rating', value: 'rating', type:'v-rating'},
        {text: 'Position/s', value: 'positions'},
        {text: 'Comments', value: 'comments'},
      ],
      players: [
        {
          name: 'Paco pepe',
          rating: 3,
          positions: 'defender',
          comments: 'too slow',
        },
        {
          name: 'Andres',
          rating: 2,
          positions: 'goalkeeper,defender',
          comments: 'good positioning',
        },
        {
          name: 'Zachary',
          rating: 5,
          positions: 'forward',
          comments: 'hat-trick per match',
        },
      ],
    }
  },
}
</script>

<style scoped>

</style>
