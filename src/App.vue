<template>
  <div id="app">
    <Headercompo v-bind:msg="msg" :handlereset="handlereset" />
    <img src="./assets/logo.png">
    <!-- <h1>{{ msg }}</h1> -->
    <h2>{{ text }}</h2>
    <button @click="handleclick">click me</button>
  </div>
</template>

<script>
import Headercompo from './components/Headercompo.vue';
export default {
  name: 'app',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      text: 'Essential Links'
    }
  },
  methods: {
    handleclick() {
      this.text = 'changed'
    },
    handlereset() {
      this.text = 'back'
    }
  },
  components: {
    Headercompo
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

}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
