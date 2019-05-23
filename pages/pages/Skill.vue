<template>
  <v-container>
    <page-title :titles="titles"></page-title>

    <v-layout wrap>
      <skill-card v-for="skill in skills" :key="skill.title" :item="skill" />
    </v-layout>

    <v-layout align-center column justify-center>
      <v-btn large color="primary" class="ma-4" nuxt to="/pages/Career">
        CAREER
      </v-btn>
    </v-layout>
  </v-container>
</template>

<script>
import PageTitle from '@/components/PageTitle'
import SkillCard from '@/components/SkillCard'

export default {
  components: {
    PageTitle,
    SkillCard
  },
  data() {
    return {
      titles: {
        title: 'SKILL',
        subTitle: '技術'
      },
      skills: [
        {
          title: '言語',
          skills: [
            { skill: 'JavaScript', period: 4, rate: 3 },
            { skill: 'Java', period: 4, rate: 2 },
            { skill: 'SQL', period: 4, rate: 2 },
            { skill: 'HTML5', period: 5, rate: 2 },
            { skill: 'Bash', period: 5, rate: 2 },
            { skill: 'PL/SQL', period: 4, rate: 2 },
            { skill: 'CSS3', period: 2, rate: 1 },
            { skill: 'PHP', period: 0.5, rate: 1 },
            { skill: 'VB.NET', period: 1, rate: 1 }
          ]
        },
        {
          title: 'フレームワーク',
          skills: [
            { skill: 'JQuery', period: 4, rate: 3 },
            { skill: 'Spring', period: 2.5, rate: 2 },
            { skill: 'Struts', period: 2, rate: 1 },
            { skill: 'Vue.js', period: 0.5, rate: 1 },
            { skill: 'Nuxt.js', period: 0.5, rate: 1 },
            { skill: 'Vuetify', period: 0.3, rate: 1 },
            { skill: 'Bootstrup', period: 0.5, rate: 1 }
          ]
        },
        {
          title: 'OS／ミドルウェア',
          skills: [
            { skill: 'Linux', period: 4, rate: 2 },
            { skill: 'Apache', period: 4, rate: 2 },
            { skill: 'ORACLE', period: 4, rate: 2 },
            { skill: 'glassfish', period: 4, rate: 2 },
            { skill: 'Tomcat', period: 4, rate: 1 },
            { skill: 'PostgreSQL', period: 1, rate: 1 }
          ]
        },
        {
          title: 'その他',
          skills: [
            { skill: 'SVN', period: 6, rate: 3 },
            { skill: 'JUnit', period: 2.5, rate: 2 },
            { skill: 'Git', period: 1, rate: 1 },
            { skill: 'Gulp', period: 1, rate: 1 },
            { skill: 'Node.js', period: 1, rate: 1 },
            { skill: 'Selenium', period: 1, rate: 1 },
            { skill: 'Netlify', period: 0.2, rate: 1 }
          ]
        }
      ]
    }
  }
}
</script>
