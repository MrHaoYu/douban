<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      {{count}}
    </div>
    <button type="button" name="button" @click="increment">加数</button>
    <router-link to="/">Home</router-link>
    <router-link to="/a">About</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
import { mapState, mapActions } from 'vuex'
export default {
  name: 'App',
  computed: mapState([
    'count'
  ]),
  methods: {
      ...mapActions([
        'increment'
      ])
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
