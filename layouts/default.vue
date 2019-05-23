<template>
  <v-app>
    <MyHeader></MyHeader>
    <v-content>
      <nuxt />
    </v-content>
    <MyFooter></MyFooter>
  </v-app>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
import MyFooter from '@/components/MyFooter.vue'

export default {
  components: {
    MyHeader,
    MyFooter
  }
}
</script>

<style>
@media only screen and (min-width: 800px) {
  .container {
    max-width: 800px;
  }
}
</style>
