<template>
  <div id="app">
    <Tree :model="treeData"/>
  </div>
</template>

<script>
import Tree from './components/Tree.vue'

export default {
  name: 'app',
  components: {
    Tree
  },
  data() {
    return {
      treeData: [{
        id: 1,
        name: 'a',
        children: [{
          id: 2,
          name: 'a-1',
          children: [{
            id: 3,
            name: 'a-1-1',
            children: [{
              id: 'a-1-1-1',
              name: 'a-1-1-1',
            }]
          }, {
            id: 4,
            name: 'a-1-2'
          }]
        }, {
          id: 5,
          name: 'a-2'
        }]
      }, {
        id: 6,
        name: 'b'
      }]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
