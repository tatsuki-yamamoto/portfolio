<template>
  <v-container>
    <page-title :titles="titles"></page-title>

    <v-layout justify-center>
      <v-card class="ma-2">
        <v-container fluid>
          <v-layout align-center column justify-center>
            <v-flex class="mb-4" xs12>
              <h4 class="subheading">
                何か問い合わせたい内容があれば、twitterのDMからお願いします。
              </h4>
            </v-flex>
            <v-flex xs12>
              <v-btn
                large
                color="light-blue"
                class="white--text text-lowercase"
                href="https://twitter.com/yama_tatsuki"
                target="_brank"
              >
                Twitterへ
              </v-btn>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-layout>

    <v-layout align-center column justify-center>
      <v-btn large color="" class="ma-4" nuxt to="/">
        TOP
      </v-btn>
    </v-layout>
  </v-container>
</template>

<script>
import PageTitle from '@/components/PageTitle'

export default {
  components: {
    PageTitle
  },
  data() {
    return {
      titles: {
        title: 'CONTACT',
        subTitle: '連絡先'
      }
    }
  }
}
</script>
