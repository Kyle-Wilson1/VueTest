<template>
<tabbar>
  <tabbar-item selected>
    <img slot="icon" src="../assets/image/1.jpg">
    <span slot="label">Home</span>
  </tabbar-item>
  <tabbar-item>
    <img slot="icon" src="../assets/image/2.jpg">
    <span slot="label">Company</span>
  </tabbar-item>
  <!-- <tabbar-item>
      <img style="height:40px;width:40px;" slot="icon" src="../assets/image/ic_nav_add_normal.png">
    </tabbar-item> -->
  <tabbar-item @on-item-click="addNumber">
    <img slot="icon" src="../assets/image/3.jpg">
    <span slot="label">Opportunity</span>
  </tabbar-item>
  <tabbar-item :badge="number" link="/1">
    <img slot="icon" src="../assets/image/4.jpg">
    <span slot="label">My</span>
  </tabbar-item>
</tabbar>
</template>
<style>
.add {
  height: 40px;
  width: 40px;
}
</style>
<script>
import {
  Tabbar,
  TabbarItem
} from 'vux'
export default {
  name: 'AppFooter',
  components: {
    Tabbar,
    TabbarItem
  },
  data () {
    return {
      msg: '',
      number: 1
    }
  },
  methods: {
    addNumber () {
      this.number = this.number + 1
    }
  }
}
</script>
