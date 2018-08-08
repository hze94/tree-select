<template>
  <li>
    <div @click="toggle">{{model.name}} <span v-if="!isLeaf">{{isOpen?'【 - 】':'【 + 】'}}</span></div>
    <Tree v-if="model.children" v-show="isOpen" :model="model.children"/>
  </li>
</template>

<script>
import Tree from './Tree.vue'
export default {
  name: 'TreeNode',
  components: { Tree },
  props: {
    model: {
      default: []
    }
  },
  data() {
    return {
      isOpen: false
    }
  },
  computed: {
    isLeaf() {
      return !this.model.children
    }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>
