<template>
  <div>
    <!-- <div class="vux-demo">
      <img class="logo" src="../assets/vux_logo.png">
    </div>
    <group title="cell demo1">
      <cell title="VUX" value="cool"  link="/1"></cell>
    </group> -->
    <appheader1></appheader1>
    <AppFooter></AppFooter>
    <panel header="job list" :footer="footer" :list="list" type="1">
      <cell title="titlesss" value="cell"></cell>
    </Panel>

  </div>
</template>

<script>
import { Group, Cell, Panel } from 'vux'
import appheader1 from './Header'
import AppFooter from './Footer'
export default {
  components: {
    Group,
    Cell,
    Panel,
    appheader1,
    AppFooter
  },
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!',
      list: [{
        src: require('../assets/image/qingtengyun.png'),
        // src: require('../assets/image/qingtengyun.png'),
        title: '青藤云安全',
        desc: 'c++开发 .<br> Location:北京',
        url: '/1',
        meta: {
          source: 'abccc'
        }
      }, {
        src: require('../assets/image/yuanchuan.jpg'),
        title: '远传技术',
        desc: 'java开发 .<br> Location:成都',
        url: '/1'
      }],
      footer: {
        title: 'more'
      }
    }
  }
}
</script>

<style>
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
