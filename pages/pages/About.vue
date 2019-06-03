<template>
  <v-container class="root">
    <page-title :titles="titles"></page-title>

    <v-layout>
      <v-flex>
        <v-card class="ma-2">
          <v-container fluid>
            <v-list>
              <v-list-tile
                v-for="item in items"
                :key="item.title"
                class="tile pa-2"
              >
                <v-layout wrap>
                  <v-flex xs12 sm4>
                    <v-list-tile-content class="subheading font-weight-bold">
                      {{ item.title }}
                    </v-list-tile-content>
                  </v-flex>
                  <v-flex xs12 sm8>
                    <v-list-tile-content class="subheading">
                      {{ item.content }}
                    </v-list-tile-content>
                  </v-flex>
                </v-layout>
              </v-list-tile>
            </v-list>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout align-center column justify-center>
      <v-btn large color="primary" class="ma-4" nuxt to="/pages/Skill">
        SKILL
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
        title: 'ABOUT',
        subTitle: '自己紹介'
      },
      items: [
        {
          title: '名前',
          content: 'yama_tatsuki'
        },
        {
          title: '出身',
          content: '大阪（東京在住）'
        },
        {
          title: '学歴',
          content: '関西大学システム理工学部 卒'
        },
        {
          title: '現在の職業',
          content: '新卒採用でメーカ系Sierへ就職。Web系SEを経験。'
        },
        {
          title: '挑戦したいこと',
          content:
            '人々の生活を１段階アップさせるようなアプリやWebサイトを作ること。そのために、向上心を忘れず、新しい技術への関心を持ち続けること。'
        },
        {
          title: 'おおまかな将来像',
          content:
            'フロントorバックエンドエンジニアを経験した後、PL・PMのようなマネジメント業務をしたいと考えています。'
        }
      ]
    }
  }
}
</script>

<style scoped>
.root >>> .tile > div {
  height: auto;
}
</style>
