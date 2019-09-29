<template>
  <div id="app">
    <Header />
    <b-tabs>
      <b-tab-item
        v-for="game in games"
        :key="game.id"
        :label="game.name"
      >
        <Game :game="game"></Game>
      </b-tab-item>
    </b-tabs>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Game from './components/Game.vue'

import games from '@/assets/games.json'

export default {
  name: 'app',
  components: {
    Header,
    Game
  },
  data () {
    return {
      games
    }
  }
}
</script>
