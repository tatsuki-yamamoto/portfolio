<template>
  <v-flex xs12 sm6 md6 d-flex>
    <v-card class="ma-2">
      <v-img :src="item.image" aspect-ratio="2.5"></v-img>

      <v-card-title class="pb-0">
        <div class="title font-weight-bold ma-2">{{ item.title }}</div>
      </v-card-title>

      <v-card-text class="pt-0 pb-0 grey--text font-weight-bold">
        {{ item.postion }}
      </v-card-text>
      <v-card-text class="pt-0 pb-0 grey--text">{{ item.skil }}</v-card-text>
      <v-card-text class="pt-0 pb-0 red--text">{{ item.piriod }}</v-card-text>

      <v-card-text>{{ item.content }}</v-card-text>
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: 'CareerCard',
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
