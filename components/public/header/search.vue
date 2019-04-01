<template>
  <div class="m-search">
    <div class="search-wrapper">
      <div class="logo">
        <img src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/logo.png" alt="">
      </div>
      <div class="header-search-module">
        <div class="header-search-block">
          <input
            @focus="handleFocus"
            @blur="handleBlur"
            v-model="search"
            class="header-search-input"
            type="text"
            placeholder="搜索商家或地址">
          <button class="header-search-btn">
            <i class="iconfont">&#xe60a;</i>
          </button>
        </div>
        <div class="header-search-suggest" v-if="isFocus">
          <div class="header-search-noinput" v-if="!search">
            <div class="header-search-history">
              <h6>最近搜索</h6>
              <span class="header-search-clean">删除搜索历史</span>
              <div class="header-search-hotword">
                <a href="">玉渊潭公园</a>
                <a href="">玉渊潭公园</a>
              </div>
            </div>
            <h6>热门搜索</h6>
            <div class="header-search-hotword">
              <a href="">玉渊潭公园</a>
              <a href="">玉渊潭公园</a>
              <a href="">玉渊潭公园</a>
              <a href="">玉渊潭公园</a>
              <a href="">玉渊潭公园</a>
              <a href="">玉渊潭公园</a>
            </div>
          </div>
          <div class="header-search-hasinput" v-if="search">
            <ul>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
              <li><a href="">爱情公寓</a></li>
            </ul>
          </div>
        </div>
        <div class="header-search-hotword" v-if="!isFocus">
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
          <a href="">玉渊潭公园</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isFocus: false,
      search: ''
    }
  },
  methods:{
    handleFocus() {
      this.isFocus = true
    },
    handleBlur(){
      this.isFocus = false
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~@/assets/css/global.scss';
.m-search{
  height: 150px;
  background-color: #ffffff;
  .search-wrapper{
    width: 1200px;
    margin: 0 auto;
  }
  .logo{
    float: left;
    padding-top: 28px;
    padding-right: 60px;
    padding-bottom: 40px;
    width: 280px;
    img{
      width: 126px;
      height: 46px;
    }
  }
  .header-search-module{
    float: left;
    padding-top: 28px;
    position: relative;
    .header-search-block{
      width: 550px;
      height: 40px;
      border: 1px solid $fc-main;
      background-color: #ffffff;
      border-radius: 4px;
      font-size: 0;
      overflow: hidden;
      box-sizing: content-box;
      .header-search-input{
        width: 462px;
        height: 100%;
        border: none;
        outline: none;
        padding: 10px;
        box-sizing: border-box;
        display: inline-block;
        font-size: 15px;
      }
      .header-search-btn{
        border: none;
        outline: none;
        width: 88px;
        height: 100%;
        box-sizing: border-box;
        display: inline-block;
        background-color: $fc-main;
        color: #ffffff;
        cursor: pointer;
      }
    }
    .header-search-suggest {
      position: absolute;
      left: 0;
      top: 70px;
      width: 462px;
      overflow: hidden;
      background: #ffffff;
      border: 1px solid $fc-9;
      border-radius: 4px;
      border-top-left-radius: 0;
      border-top-right-radius: 0;
      border-top: none;
      box-sizing: border-box;
      h6{
        font-size: $fs-13;
        margin: 0;
        margin-top: 8px;
      }
      .header-search-noinput{
        padding-left: 10px;
        padding-bottom: 10px;
        box-sizing: border-box;
        .header-search-clean{
          position: absolute;
          right: 10px;
          top: 10px;
          color: $fc-c;
          font-size: $fs-10;
          cursor: pointer;
        }
      }
      .header-search-hasinput {
        li{
          a{
            color: $fc-9;
            line-height: 25px;
            display: block;
            text-indent: 10px;
            &:hover{
              color: $fc-main;
              background-color: $fc-e;
            }
          }
        }
      }
    }
    .header-search-hotword{
      padding-top: 8px;
      font-size: $fs-12;
      width: 550px;
      height: 25px;
      box-sizing: border-box;
      text-align: left;
      padding-left: 12px;
      a{
        color: $fc-9;
        margin-right: 10px;
        margin-bottom: 3px;
        display: inline-block;
      }
    }
  }
}
</style>
