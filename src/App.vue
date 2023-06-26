<template>
  <h1 :classvar="{'title':true, 'title-home':isHome}">FastFoodX</h1>
  <div class="user" v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>

  <div class="option">
    <div v-if="accessLevel === Admin">User Admin</div>
    <div v-else-if="accessLevel === Marketing">User Marketing</div>
    <div v-else="accessLevel === User">normal User</div>
  </div>

  <formulary></formulary>
  <cabeca v-if="showHeader"/>


  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import cabeca from './components/cabeca.vue'
import formulary from './components/formulary.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    cabeca,
    formulary
  },
  data(){
    return{
      showHeader: true,
      firstName: 'Selmo',
      lastName: 'Selmura',
      showName: true,
      accessLevel: 'Marketing',
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
