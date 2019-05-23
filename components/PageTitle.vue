<template>
  <v-layout align-center justify-center column>
    <v-flex xs12>
      <h2 class="display-1 font-weight-black mt-3 indigo--text">
        {{ titles.title }}
      </h2>
    </v-flex>
    <v-flex xs12>
      <h3 class="title font-weight-black mb-3 grey--text">
        {{ titles.subTitle }}
      </h3>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: 'PageTitle',
  props: {
    titles: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
