<template>
  <v-flex class="root" xs12 sm6 d-flex>
    <v-card class="ma-2">
      <v-card-title class="pb-0">
        <div class="headline font-weight-bold ma-2">{{ item.title }}</div>
      </v-card-title>
      <v-container fluid>
        <v-list dense>
          <v-list-tile
            v-for="skill in item.skills"
            :key="skill.title"
            :item="skill"
            class="tile"
          >
            <v-layout wrap>
              <v-flex xs8 md4>
                <v-list-tile-content
                  class="align-start subheading font-weight-medium"
                >
                  {{ skill.skill }}
                </v-list-tile-content>
              </v-flex>
              <v-flex xs4 md2>
                <v-list-tile-content class="align-end">
                  {{ skill.period | toFixed }}年
                </v-list-tile-content>
              </v-flex>
              <v-flex md6 class="hidden-sm-and-down">
                <v-list-tile-content class="align-end">
                  <v-rating v-model="skill.rate" length="3"></v-rating>
                </v-list-tile-content>
              </v-flex>
            </v-layout>
          </v-list-tile>
        </v-list>
      </v-container>
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: 'SkillCard',
  filters: {
    toFixed: function(num) {
      return num.toFixed(1)
    }
  },
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style scoped>
.root >>> .tile > div {
  height: 30px;
}
.root >>> .align-end {
  align-items: flex-end;
}
</style>
