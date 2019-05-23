<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      clipped
      app
      disable-resize-watcher
      width="200"
    >
      <v-toolbar color="teal" flat>
        <v-list class="pa-0">
          <v-list-tile nuxt to="/">
            <v-list-tile-title class="white--text title">
              {{ title }}
            </v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-toolbar>

      <v-divider></v-divider>

      <v-list class="pt-0" dense three-line>
        <v-list-tile v-for="item in items" :key="item.to" nuxt :to="item.to">
          <v-list-tile-content>
            <v-list-tile-title>{{ item.label }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar class="header" color="teal" fixed app>
      <v-toolbar-side-icon
        class="white--text hidden-sm-and-up"
        @click.stop="drawer = !drawer"
      ></v-toolbar-side-icon>
      <v-layout justify-center fill-height>
        <v-toolbar-items class="hidden-xs-only">
          <v-btn
            v-for="item in items"
            :key="item.to"
            class="white--text"
            :to="item.to"
            flat
            nuxt
          >
            {{ item.label }}
          </v-btn>
        </v-toolbar-items>
      </v-layout>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  name: 'MyHeader',
  data: () => ({
    items: [
      {
        to: '/',
        label: 'Top'
      },
      {
        to: '/pages/About',
        label: 'About'
      },
      {
        to: '/pages/Skill',
        label: 'Skill'
      },
      {
        to: '/pages/Career',
        label: 'Career'
      },
      {
        to: '/pages/Works',
        label: 'Works'
      },
      {
        to: '/pages/Contact',
        label: 'Contact'
      }
    ],
    drawer: false,
    title: 'Portfolio'
  })
}
</script>
