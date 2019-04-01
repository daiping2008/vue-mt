<template>
  <div class="m-user">
    <template v-if="user">
      欢迎您，<span class="username">{{user}}</span>
      <nuxt-link to="/exit">退出</nuxt-link>
    </template>
    <template v-else>
      <nuxt-link to="/login" class="login">
        立即登录
      </nuxt-link>
      <nuxt-link to="/register" class="register">
        注册
      </nuxt-link>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user:''
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~@/assets/css/global.scss';
.m-user{
  font-size: $fs-12;
  color: $fc-9;
  float: left;
  margin-left: 20px;
  .login{
    color: $fc-main;
  }
  .register{
    color: $fc-9;
    margin-left: 5px;
    &:hover {
      color: $fc-main;
    }
  }
}
</style>

