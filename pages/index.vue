<template>
  <v-parallax :src="require('assets/img/background.jpg')" height="600">
    <v-layout align-center column justify-center>
      <h1 class="display-1 indigo--text font-weight-bold">
        This is yama_tatsuki's Portfolio
      </h1>
      <v-btn large color="primary" class="ma-4" nuxt to="/pages/About">
        About
      </v-btn>
    </v-layout>
  </v-parallax>
</template>
