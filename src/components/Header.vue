<template>
  <!--<div class="tabbar">
    <div class="title">{{title}}</div>
  </div>-->



  <div class="tabbarr">
    <div class="title">{{title}}</div>
    <tabbar-item class="search">
      <img slot="icon" src="../assets/image/search.png">
    </tabbar-item>
    <!-- <tabbar-item>
      <img slot="icon" src="../assets/image/2.jpg">
      <span slot="label">Company</span>
    </tabbar-item> -->
  </div>


</template>
<style>
.search{
position:absolute;right:5px;top:5px;z-index:999;
}
.title{
   text-align:center;
   margin:auto;
   color:white;
   line-height:50px;
   font-size:18px;
}
.tabbarr{
   background-color:RGB(79,175,140);
   height:50px;
   position:relative;
}
</style>
<script>
import { Tabbar, TabbarItem } from 'vux'
export default {
  name: 'AppHeader',
  components: {
    Tabbar,
    TabbarItem
  },
  data () {
    return {
      title: 'Recommend'
    }
  },
  methods: {
    resultClick (item) {
      alert('you click the result item: ' + JSON.stringify(item))
    },
    getResult (val) {
      this.results = val
    }
  }
}

</script>
