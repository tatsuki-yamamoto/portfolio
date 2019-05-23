<template>
  <v-container grid-list-sm>
    <page-title :titles="titles"></page-title>

    <v-layout justify-center wrap>
      <career-card v-for="job in jobs" :key="job.title" :item="job" />
    </v-layout>

    <v-layout align-center column justify-center>
      <v-btn large color="primary" class="ma-4" nuxt to="/pages/Contact">
        WORKS
      </v-btn>
    </v-layout>
  </v-container>
</template>

<script>
import PageTitle from '@/components/PageTitle'
import CareerCard from '@/components/CareerCard'

export default {
  components: {
    PageTitle,
    CareerCard
  },
  data() {
    return {
      titles: {
        title: 'CAREER',
        subTitle: '業務経歴'
      },
      jobs: [
        {
          title: '銀行ポータルサイト',
          image: require('assets/img/bank.jpg'),
          postion: 'PL, 要件定義, 設計, 実装, テスト, 保守',
          piriod: '2016~2019',
          skil: 'Java(Spring), JavaScript, JQuery, Bash, ORACLE',
          content:
            '銀行向けの各種保険・ローン申し込み機能(火災保険/住宅/カード等)、顧客マイページ機能、管理者機能の開発・保守を実施。PLとしてメンバーの統制および主にフロントの開発を担当。'
        },
        {
          title: '畜産・酪農器具リースシステム',
          image: require('assets/img/cow.jpg'),
          postion: '設計, 実装, テスト',
          piriod: '2015~2016',
          skil: 'VB.NET, ORACLE',
          content:
            'WindowsOSサポート切れにともなう畜産農家への資材（トラクター等）のリース管理機能のマイグレーションを実施。新規画面の開発等を担当。'
        },
        {
          title: '中古車販売ポータルサイト',
          image: require('assets/img/car.jpg'),
          postion: '設計, 実装, テスト',
          piriod: '2014',
          skil: 'HTML5, CSS3, JavaScript, JQuery, ORACLE, PHP',
          content:
            '中古車・中古船舶の検索サイト、サイト管理機能、加盟店管理機能のリニューアルを実施。主にフロントの開発を担当。'
        },
        {
          title: '給与明細照会サービス',
          image: require('assets/img/salary.jpg'),
          postion: '設計, 実装, テスト',
          piriod: '2013',
          skil: 'Java(Struts), Apache, Tomcat, PostgreSQL',
          content:
            'PC／スマートフォンから給与明細を閲覧するSaaSサービス。新規画面の開発等を担当。'
        }
      ]
    }
  }
}
</script>
