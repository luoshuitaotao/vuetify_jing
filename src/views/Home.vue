<template>
  <div class="home">
    <h1>HomePage</h1>
    <v-btn class="pink white--text">Click me</v-btn>
    <v-btn depressed color="pink">Click me</v-btn>
    <v-btn rounded color="pink">Click ME</v-btn>
    <v-btn flat color="pink">Click ME</v-btn>


    <v-btn depressed class="pink white--text">
      <v-icon left>mdi-email</v-icon>
      <span>Email me</span>
    </v-btn>

    <v-btn depressed  small class="pink white--text">
      <v-icon left>mdi-email</v-icon>
      <span>Email me</span>
    </v-btn>

    <v-btn depressed large class="pink white--text">
        <span>Email me</span>
        <v-icon right>mdi-email</v-icon>
    </v-btn>

    <v-btn depressed small fab dark color="purple">
        <v-icon>mdi-heart</v-icon>
    </v-btn>
    </div>
</template>

<script>
// @ is an alias to /src

export default {
}
</script>
