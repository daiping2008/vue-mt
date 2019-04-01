<template>
  <div class="m-geo">
    <i class="iconfont geo-location">&#xe6c1;</i>
    <span class="current-city">北京市</span>
    <nuxt-link class="changeCity" to="changeCity">切换城市</nuxt-link>
    [<a class="city-guess">天津</a><a class="city-guess">天津</a><a class="city-guess">天津</a>]
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '~@/assets/css/global.scss';

.m-geo{
  color: $fc-9;
  font-size: $fs-12;
  float: left;
  .geo-location{
    color: $fc-6;
    font-size: 12px;
  }
  .current-city{
    color: $fc-6;
  }
  .changeCity{
    color: $fc-6;
    border: 1px solid $fc-9;
    padding:0 2px;
    &:hover{
      color: $fc-main;
    }
  }
  .city-guess{
    color: $fc-9;
    margin: 0 4px;
    &:hover{
      color: $fc-main;
    }
  }
}
</style>
