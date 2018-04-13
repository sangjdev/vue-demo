<template>
    <header>
        <h1 v-on:click="changeTitle">{{title}}</h1>
    </header>
</template>

<script>
import {bus} from '../main';

export default {  
  props: {
    title: {
      type: String
    }
  },
  data () {
    return {
      title: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    changeTitle: function () {
      // this.$emit('changeTitle', 'Vue Wizrds')
      this.title = 'Vue Wizards'
      bus.$emit('titleChanged','Vue Wizards');
    }
  }
}
</script>

<style>
header {
  background: lightgreen;
  padding: 10px;
}
h1 {
  color: #222;
  text-align: center;
}
</style>
