<template>
  <div id="app">
    <Header />
    <b-tabs expanded>
      <b-tab-item
        v-for="game in games"
        :key="game.id"
      >
        <template slot="header">
          <img
            :src="'logos/' + game.id + '.png'"
            class="logo"
          />
        </template>
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

<style>
@media only screen and (min-width: 960px) {
  .logo {
    height: 64px;
  }
}

@media only screen and (min-width: 580px) and (max-width: 960px) {
  .logo {
    height: 32px;
  }
}

@media only screen and (max-width: 580px) {
  .logo {
    height: 16px;
  }
}
</style>
