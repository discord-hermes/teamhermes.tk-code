<template>
  <div id="app">
    <sui-menu fixed borderless>
      <sui-menu-item>Team Hermes</sui-menu-item>
      <sui-menu-menu position="right">
        <a 
        is="sui-menu-item" 
        v-for="item in items" 
        :content="item"  
        />
      </sui-menu-menu>
    </sui-menu>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        items: [
        "팀 소개",
        "프로젝트",
        "봇 설치"
        ]
      }
    },
    components: {
    }
  }
</script>

<script>
  alert('dark 바보')
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
