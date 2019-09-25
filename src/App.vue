<template>
  <div id="app">
    <Navbar />
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
import Navbar from './components/Navbar.vue'
import Game from './components/Game.vue'

import games from '@/assets/games.json'

export default {
  name: 'app',
  components: {
    Navbar,
    Game
  },
  data () {
    return {
      games
    }
  }
}
</script>
