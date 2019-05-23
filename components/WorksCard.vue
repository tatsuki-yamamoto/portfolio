<template>
  <v-flex xs12 sm6 md6 d-flex>
    <v-hover>
      <v-card class="ma-2" hover :href="item.site" target="_brank" ripple>
        <v-img :src="item.image" aspect-ratio="1.4"></v-img>

        <v-card-title class="pb-0">
          <div class="title font-weight-bold ma-2">{{ item.title }}</div>
        </v-card-title>

        <v-card-text class="pt-0 pb-0 grey--text">{{ item.skil }}</v-card-text>

        <v-card-text class="pb-0">{{ item.content }}</v-card-text>

        <v-card-actions>
          <v-btn flat color="orange" :href="item.sauce" target="_brank">
            SAUCE CODE
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-hover>
  </v-flex>
</template>

<script>
export default {
  name: 'WorksCard',
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
