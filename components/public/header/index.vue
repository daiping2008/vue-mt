<template>
  <div class="m-header clearfix">
    <div class="top-bar">
      <geo/>
      <user/>
      <my-nav/>
    </div>
    <search/>
  </div>
</template>

<script>
import Geo from './geo'
import User from './user'
import MyNav from './nav'
import Search from './search'

export default {
  components: {
    Geo,
    User,
    MyNav,
    Search
  }
}
</script>

<style lang="scss" scoped>
.m-header{
  .top-bar{
    width: 1200px;
    margin: 0 auto;
    height: 40px;
    line-height: 40px;
    .top-wrapper{
      width: 1190px;
      margin: 0 auto;
    }
  }
}
</style>

