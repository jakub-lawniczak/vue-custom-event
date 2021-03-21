<template>
  <div id="app">
    <h2>{{ title }}</h2>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld :title="title" @addTitle="addTitle($event)"/>
    <hr>
    <TitleChanger :title="title" @changeTitle="changeTitle($event)"></TitleChanger>
    <hr>
    <CustomTitle :title="title" @customTitle="customTitle($event)"></CustomTitle>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TitleChanger from './components/TitleChanger.vue'
import CustomTitle from './components/CustomTitle.vue'

export default {
  name: 'App',
  data() {
    return {
      title: 'Hello World'
    }
  },
  components: {
    HelloWorld,
    TitleChanger,
    CustomTitle
  },
  methods: {
    addTitle(value) {
      this.title = value;
    },
    changeTitle(value) {
      this.title = value;
    },
    customTitle(value) {
      this.title = value;
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
