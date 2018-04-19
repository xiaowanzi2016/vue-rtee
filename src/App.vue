<template>
  <div  id="app">
    <ul>
      <tree-menu     v-for="(item,index) in tree "  :data="item" :key="index" ></tree-menu>
    </ul>
  </div>
</template>

<script>
import TreeMenu from './components/HelloWorld'
var data = [
  {
    lable: 'root',
    nodes: [
      {
        lable: 'item1',
        nodes: [
          {
            lable: 'item1.1'
          },
          {
            lable: 'itemm1.2',
            nodes: [
              {
                lable: 'item1.2.1'
              }
            ]

          }
        ]

      },
      {
        lable: 'item2'
      }
    ]
  }
]

export default{
  data: function () {
    return {
      tree: data
    }
  },
  components: {
    TreeMenu
  }
}
</script>
