<template>
  <div id="app">
    <Landing-page></Landing-page>
  </div>
</template>

<script>
import LandingPage from './components/LandingPage'

export default {
  name: 'app',
  components: {
    LandingPage
  }
}
</script>

<style>
*{
  padding:0;
  margin:0;
  box-sizing: border-box;
}
div, p, span, h1, h2, h3, h4, td{
  font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
}
#app {
  height:100%;
}
body,html{
  height:100%;
}
</style>
