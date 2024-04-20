<template>
  <v-dialog max-width="500px">
    <template v-slot:activator="{ props: activatorProps }">
      <v-btn v-bind="activatorProps" color="surface-variant" text="Ajouter un vote" variant="flat" class="ma-5"></v-btn>
    </template>
    <template v-slot:default="{ isActive }">
      <v-card>
        <v-form>
          <v-text-field label="Nom"></v-text-field>
          <v-text-field label="Contact"></v-text-field>
          
          <v-autocomplete label="Vote 1"></v-autocomplete>
          <v-autocomplete label="Vote 2"></v-autocomplete>
          <v-autocomplete label="Vote 3"></v-autocomplete>
        </v-form>
        <v-btn text="À voter!" @click="isActive.value = false"></v-btn>
      </v-card>
    </template>
  </v-dialog>
</template>

<script>
export default {
  name: 'VoteForm',
}
</script>