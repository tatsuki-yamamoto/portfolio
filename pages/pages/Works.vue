<template>
  <v-container grid-list-sm>
    <page-title :titles="titles"></page-title>

    <v-layout class="mb-3" justify-center wrap>
      <works-card v-for="work in works" :key="work.title" :item="work" />
    </v-layout>

    <v-layout align-center column justify-center>
      <v-btn large color="primary" class="ma-4" nuxt to="/pages/Contact">
        CONTACT
      </v-btn>
    </v-layout>
  </v-container>
</template>

<script>
import PageTitle from '@/components/PageTitle'
import WorksCard from '@/components/WorksCard'

export default {
  components: {
    PageTitle,
    WorksCard
  },
  data() {
    return {
      titles: {
        title: 'WORKS',
        subTitle: '作品'
      },
      works: [
        {
          title: 'Portfolioサイト',
          image: require('assets/img/portfolio.png'),
          skil: 'JavaScript, Vue.js, Nuxt.js, Vuetify',
          content:
            '個人的に勉強したVue.jsを用いてポートフォリオサイトを作成しました。デザインはVuetifyを使用しています。',
          site: '/',
          sauce: 'https://github.com/tatsuki-yamamoto/portfolio'
        },
        {
          title: '入力フォーム①',
          image: require('assets/img/vue-form-sample.png'),
          skil: 'JavaScript, Vue.js, Bootstrap, VueCLI',
          content:
            'Vue.jsで作成した入力フォームのサンプルページです。仕事で開発している入力フォームのSPA化のために作成しました。',
          site: 'https://vue-form-sample.netlify.com/spa/vuecli',
          sauce: 'https://github.com/tatsuki-yamamoto/vue-form-sample'
        },
        {
          title: '入力フォーム②',
          image: require('assets/img/vue-form-sample2.png'),
          skil: 'JavaScript, Vue.js, Bootstrap',
          content:
            'Vue.jsで作成した入力フォームのサンプルページです。ビルドツールを使用せず作成しました。',
          site: 'https://vue-form-sample2.netlify.com/spa/vue',
          sauce: 'https://github.com/tatsuki-yamamoto/portfolio'
        }
      ]
    }
  }
}
</script>
