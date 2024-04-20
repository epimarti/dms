<template>
  <v-app>

    <v-app-bar app>
      <!-- <v-toolbar-title>Deadpool</v-toolbar-title> -->
      
      <v-tabs v-model="tab">
        <v-tab key="deadpool" value="deadpool">Deadpool</v-tab>

        <v-tab key="winners" value="winners">Gagnants</v-tab>
      </v-tabs>

      <v-spacer></v-spacer>

      <v-menu>
        <template v-slot:activator="{ props }">
          <v-btn icon v-bind="props">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item>
            <v-list-item-title>Import</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Export</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Check</v-list-item-title>
          </v-list-item>

          <v-list-item style="background-color: red;">
            <v-list-item-title>Reset</v-list-item-title>
          </v-list-item>
        </v-list>

      </v-menu>
    </v-app-bar>
    <v-main>
      <v-window v-model="tab">
        <v-window-item key="deadpool" value="deadpool">
          <DeadPool />
        </v-window-item>
        <v-window-item key="winners" value="winners">
          <Winners />
        </v-window-item>
      </v-window>
    </v-main>
  </v-app>
</template>

<script>
import DeadPool from './components/Deadpool.vue'
import Winners from './components/Winners.vue'

export default {
  name: 'App',

  components: {
    DeadPool,
    Winners
  }
  ,
  data: () => ({
    tab: null
  }),
}
</script>
