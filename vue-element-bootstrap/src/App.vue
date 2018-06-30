<template>
  <div id="app">
    <header-view/>
    <div class='main'>
      <router-view/>
    </div>
  </div>
</template>

<script>
import HeaderView from '@/components/HeaderView';

export default {
  name: 'App',
  components: {
    HeaderView,
  },
};
</script>

<style lang="scss" scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    padding: 10px;
    min-width: 1400px;
  }
  .main {
    margin-top: 20px;
    .router-view {
      margin: auto;
      font-size: 14px;
    }
  }
</style>
