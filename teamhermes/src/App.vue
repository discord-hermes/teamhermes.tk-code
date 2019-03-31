<template>
  <div id="app">
    <sui-menu fixed borderless>
      <sui-container>
        <sui-menu-item>Team Hermes</sui-menu-item>
        <sui-menu-menu position="right">
          <a 
          is="sui-menu-item" 
          v-for="item in items" 
          :content="item.title" 
          :href="'#' + item.id"
          />
        </sui-menu-menu>
      </sui-container>
    </sui-menu>
    <p :style="{fontSize: '100px', fontWeight: '700'}">
      Team Hermes
    </p>
    <h1 
    is="sui-header"
    v-for="item in items" 
    :content="item.title" 
    :id="item.id"/>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        items: [
        {title: "팀 소개", id: "team"},
        {title: "프로젝트", id: "project"},
        {title: "봇 추가", id: "add"}
        ]
      }
    },
    components: {
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
    margin-top: 41.6px;
  }
</style>
