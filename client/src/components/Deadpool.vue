<template>
  <VoteForm />
  <v-spacer></v-spacer>
  <v-container fluid>
    <v-row>
      <v-col v-for="celebrity of celebrities" :key="celebrity.id" cols="auto" class="align-self-stretch">

        <v-card width="300px" height="100px">
          <MournRibbon v-if="celebrity.dateOfDeath" />
          <v-card-item>
            <template v-slot:append>
              <v-badge :content="celebrity.votes" inline class="justify-end">
              </v-badge>
            </template>
            <v-card-title>{{ celebrity.name }}</v-card-title>
          </v-card-item>
          <v-card-text>
            <span v-if="celebrity.dateOfDeath">{{ celebrity.dateOfDeath }}</span>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>

import MournRibbon from './MournRibbon.vue'
import VoteForm from './VoteForm.vue';
export default {
  name: 'DeadPool',
  components: {
    MournRibbon,
    VoteForm
  },
  data: () => ({
    celebrities: [
      {
        id: 1,
        name: 'Clint Eastwwod',
        votes: 15,
      }, {
        id: 2,
        name: 'Patrick Poivre D\'Arvor',
        votes: 12,
      }, {
        id: 3,
        name: 'Jacques Chirac',
        votes: 9,
        dateOfDeath: '26 septembre 2019'
      }, {
        id: 4,
        name: 'Bernadette Chirac',
        votes: 7,
      }, {
        id: 5,
        name: 'Sean Connery',
        votes: 10,
        dateOfDeath: '31 October 2020'
      }, {
        id: 5,
        name: 'Jeanne Moreau',
        votes: 10,
      }
    ]
  }),
}
</script>
