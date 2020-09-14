<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">Dashboard</h1>
    <v-container class="my-5">
      <v-card flat class="pa-3">
        <v-layout row wrap>
          <v-flex xs="12" md="6">
            <div class="caption grey--text">Project title</div>
            <div>Create a new website</div>
          </v-flex>
          <v-flex xs="6" sm="4" md="2">
            <div class="caption grey--text">Person</div>
            <div>The Net Jing</div>
          </v-flex>
          <v-flex xs="6" sm="4" md="2">
            <div class="caption grey--text">Due by</div>
            <div>1st Jan 2020</div>
          </v-flex>
          <v-flex xs="2" sm="4" md="2">
            <div class="caption grey--text">Status</div>
            <div>ongoing</div>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
}
</script>
