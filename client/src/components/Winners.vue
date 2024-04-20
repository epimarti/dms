<template>
  <v-container class="d-inline-flex justify-start">
      <v-card v-for="winner of winners" :key="winner.id" min-width="200px" class="mr-5">
        <v-card-item>
          <v-card-title>{{ winner.name }}</v-card-title>
        </v-card-item>
        <v-card-text>
          <v-list>
            <v-list-item>{{ winner.vote1 }}</v-list-item>
            <v-list-item>{{ winner.vote2 }}</v-list-item>
            <v-list-item>{{ winner.vote3 }}</v-list-item>
          </v-list>
        </v-card-text>
      </v-card>
  </v-container>
</template>

<script>

export default {
  name: 'WinnersView',

  data: () => ({
    winners: [{
      id: '1',
      name: 'Pierre',
      contact: 'non',
      vote1: 'a',
      vote2: 'b',
      vote3: 'c',
    }, {
      id: '2',
      name: 'Paul',
      contact: 'non',
      vote1: 'a',
      vote2: 'd',
      vote3: 'e',
    }, {
      id: '3',
      name: 'Jacque',
      contact: 'non',
      vote1: 'd',
      vote2: 'e',
      vote3: 'f',
    }]
  })
}
</script>