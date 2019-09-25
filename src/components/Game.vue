<template>
  <b-tabs
    expanded
    type="is-toggle-rounded"
  >
    <b-tab-item
      v-for="stat in game.stats"
      :key="stat.id"
      :label="stat.name"
    >
      <Stats :stat="stat"></Stats>
    </b-tab-item>
  </b-tabs>
</template>

<script>
import Stats from '@/components/Stats.vue'

export default {
  name: 'Game',
  components: {
    Stats
  },
  props: {
    game: {
      type: Object,
      required: true
    }
  }
}
</script>
