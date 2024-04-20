<template>
  <v-container class="d-inline-flex justify-start">
    <v-row>
      <v-col v-for="winner of winners" :key="winner.id" cols="auto">
        <v-card width="200px">
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
      </v-col>
    </v-row>
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
      vote1: 'Jacques Chirac',
      vote2: 'Sean Connery',
      vote3: 'Jeanne Moreau',
    }, {
      id: '2',
      name: 'Paul',
      contact: 'non',
      vote1: 'Jacques Chirac',
      vote2: 'Sean Connery',
      vote3: 'Jeanne Moreau',
    }, {
      id: '3',
      name: 'Jacque',
      contact: 'non',
      vote1: 'Jacques Chirac',
      vote2: 'Sean Connery',
      vote3: 'Jeanne Moreau',
    }]
  })
}
</script>