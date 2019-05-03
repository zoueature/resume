<template>
  <div id="app">
    <Experience></Experience>
    <Info></Info>
  </div>
</template>

<script>
import Info from './components/Info.vue'
import Experience from './components/Experience'

export default {
  name: 'eature',
  components: {
    Info,
    Experience
  }
}
</script>

<style>
  body {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
  }
  #app {
    position: absolute;
    width: 100%;
    height: 100%;
    left: 0;
    right: 0;
    margin: auto;
    max-width: 800px;
    background: #007cec;
    border: 1px solid #007cec;
    border-top: none;
    border-bottom: none;
  }
  .item-title {
    font-size: 16px;
  }
  @keyframes flyLeft {
    from{right: -1000px}
    to{right: 0}
  }
  @keyframes processUp {
    from{width: 0}
    to{width: 100%}
  }
</style>
