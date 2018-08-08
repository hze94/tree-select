<template>
  <ul class="tree">
    <TreeNode v-for="item in model" :key="item.id" :model="item"/>
  </ul>
</template>

<script>
// import TreeNode from './TreeNode.vue'

export default {
  name: 'Tree',
  components: { TreeNode: ()=> import('./TreeNode.vue') },
  props: {
    model: {
      type: Array,
      default: [],
      required: true
    }
  },
  data() {
    return {
      
    }
  }
}
</script>
