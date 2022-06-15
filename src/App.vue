<template>
  <div id="app">
    <MyHeader/>
    <MyMain/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyHeader, MyMain,
  }
}
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
