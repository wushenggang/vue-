<template>
  <div id="app">
    <Nav/>
    <router-view class="Right"></router-view>
  </div>
</template>

<script>
import Nav from './components/Nav'
export default {
  name: 'App',
  components: {
    Nav
  }
}
</script>

<style scoped>
  .Right{
    width: calc(100vw - 160px);
    margin-left: 160px;
  }
</style>
