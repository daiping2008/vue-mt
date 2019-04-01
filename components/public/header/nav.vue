<template>
  <div class="m-nav">
    <ul class="clearfix">
      <li class="nav-item has-child">我的美团
        <dl class="header-nav-my">
          <dd>我的订单</dd>
          <dd>我的收藏</dd>
          <dd>抵用券</dd>
          <dd>账户设置</dd>
        </dl>
      </li>
      <li class="nav-item">手机APP</li>
      <li class="nav-item has-child">商家中心
        <dl class="header-nav-merchant">
          <dd>登录商家中心</dd>
          <dd>美团智能收银</dd>
          <dd>我想合作</dd>
          <dd>手机免费开店</dd>
          <dd>餐饮代理商招募</dd>
          <dd>商家申请开票</dd>
          <dd>免费合作美团排队</dd>
        </dl>
      </li>
      <li class="nav-item has-child">网站导航
        <div class="header-nav-site">
          <dl class="header-jiulv header-nav-third">
            <dt>酒店旅游</dt>
            <dd>国际机票</dd>
            <dd>火车票</dd>
            <dd>榛果民宿</dd>
            <dd>经济型酒店</dd>
            <dd>主题酒店</dd>
            <dd>商务酒店</dd>
            <dd>公寓</dd>
            <dd>豪华酒店</dd>
            <dd>客栈</dd>
            <dd>青年旅社</dd>
            <dd>度假酒店</dd>
            <dd>别墅</dd>
            <dd>农家院</dd>
          </dl>
          <dl class="meishi header-nav-third">
            <dt>吃美食</dt>
            <dd>烤鱼</dd>
            <dd>烧烤</dd>
            <dd>自助餐</dd>
            <dd>火锅</dd>
            <dd>代金券</dd>
          </dl>
          <dl class="dianying header-nav-third">
            <dt>看电影</dt>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
          </dl>
          <dl class="app header-nav-third">
            <dt>手机应用</dt>
            <dd><img src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png" alt=""></dd>
            <dd><img src="//s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/waimai.png" alt=""></dd>
            <dd><img src="//s0.meituan.net/bs/fe-web-meituan/404d350/img/appicons/zhenguo.png" alt=""></dd>
            <dd><img src="//s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/dianping.png" alt=""></dd>
            <dd><img src="//s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/maoyan.png" alt=""></dd>
          </dl>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '~@/assets/css/global.scss';

.m-nav{
  list-style: none;
  float: right;
  .nav-item{
    position: relative;
    z-index: 99;
    text-align: center;
    font-size: $fs-12;
    width: 78px;
    float: left;
    cursor: pointer;
    border: 1px solid transparent;
    color: $fc-9;
    &:hover{
      color: $fc-main;
    }
    &.has-child{
      &:hover{
        background-color: #ffffff;
        border-left: 1px solid #e5e5e5;
        border-right: 1px solid #e5e5e5;
        box-shadow: 0 3px 5px 0 rgba(0,0,0,.1);
      }
      &:hover .header-nav-my,
      &:hover .header-nav-merchant,
      &:hover .header-nav-site{
        display: block;
      }
    }
  }
  .header-nav-my,
  .header-nav-merchant,
  .header-nav-site {
    position: absolute;
    display: none;
    border: 1px solid #e5e5e5;
    box-shadow: 0 3px 5px 0 rgba(0,0,0,.1);
    background-color: #ffffff;
    border-radius: 4px;
    border-top-right-radius: 0px;
    &::after{
      content: '';
      position: absolute;
      left: 0;
      top: -1px;
      width: 100%;
      height: 1px;
      background-color: #ffffff;
    }
    dd{
      padding: 0;
      margin: 0;
      text-align: center;
      color: $fc-9;
      cursor: pointer;
      &:hover{
        color: $fc-main;
      }
    }
  }
  .header-nav-my{
    width: 100%;
    left: -1px;
    border-top-left-radius: 0px;
  }
  .header-nav-merchant{
    width: 140%;
    right: -1px;
  }
  .header-nav-site{
    width: 1120px;
    right: -1px;
    padding: 30px 36px 36px 47px;
    box-sizing: border-box;
    .header-nav-third{
      text-align: center;
      float: left;
      margin-right: 47px;
      dt{
        margin-bottom: 25px;
      }
      dd{
        float: left;
        line-height: 30px;
      }
      &.header-jiulv{
        width: 234px;
        dd{
          width: 33.3%;
        }
      }
      &.meishi{
        width: 156px;
        dd{
          width: 50%;
        }
      }
      &.dianying{
        width: 90px;
        dd{
          width: 100%;
        }
      }
      &.app{
        float: right;
        margin-right: 0;
        dd{
          margin: 0 8px;
        }
        img{
          width: 60px;
          height: 60px;
        }
      }
    }
  }

}
</style>

