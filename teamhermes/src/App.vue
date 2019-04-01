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
    <div v-for="item in items" :id="item.id">
      <h1 is="sui-header">
        {{item.title}}
      </h1>
      <div class="description" :is="item.id"/>
    </div>
  </div>
</template>

<script>
  import team from './components/team.vue'
  import project from './components/project.vue'
  import add from './components/add.vue'

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
      team,
      project,
      add
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Noto+Sans+KR:500,900&subset=korean');
  #app {
    font-family: 'Noto Sans KR', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 41.6px;
  }
  .description {
    margin: 20px;
  }
</style>
