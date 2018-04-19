<template>
  <div class="tree">
      <li >
        <span @click="toggle" >
          <i class="fa" :class="data.nodes && data.nodes.length ? 'fa-align-center': 'fa fa-file-o' "></i>
          {{data.lable}}
        </span>
      </li>
      <ul>
        <tree-menu v-show="open"  v-for="(item,index) in data.nodes " :data="item" :key="index"></tree-menu>
      </ul>
  </div>
</template>
<script>
export default {
  props: ['data'],
  name: 'tree-menu',
  data: function () {
    return {
      theFold: [],
      open: false

    }
  },
  methods: {
    toggle: function () {
      this.open = !this.open
    }
  }
}
</script>
<style>
ul{
  list-style: none;
}
</style>
