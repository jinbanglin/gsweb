<template>
  <div class="navbar">
    <div class="navbar__logo">
      <nuxt-link to="/">挂书</nuxt-link>
    </div>
    <div class="navbar__nav">
      <nuxt-link to="/">首页</nuxt-link>
      <nuxt-link to="/trend">动态</nuxt-link>
      <nuxt-link to="/gs">开始挂书</nuxt-link>
      <nuxt-link to="/game">游戏</nuxt-link>
    </div>
    <div class="navbar__search">
      <el-input
        v-model="searchKeywords"
        size="medium"
        placeholder="搜索···"
        prefix-icon="el-icon-search"
      />
    </div>
    <div class="navbar__sub-nav">
      <nuxt-link to="/gs">
        <img src="~/assets/images/index/icon_vip.png" />
      </nuxt-link>
      <nuxt-link to="/gs">
        <img src="~/assets/images/index/icon_tips.png" />
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchKeywords: ''
    }
  }
}
</script>

<style lang="less" scoped>
@import '~/assets/styles/var.less';
.navbar {
  height: 59px;
  display: flex;
  align-items: center;

  &__logo {
    color: @textColor;
    font-size: 31px;
    font-weight: bold;
    margin-right: 108px;

    a {
      color: @textColor;
      text-decoration: none;
    }
  }

  &__nav {
    flex: 1;

    a {
      color: #555555;
      text-decoration: none;
      padding: 0 21px;
    }

    .nuxt-link-active {
      color: @textColor;
      font-weight: 500;
    }
  }

  &__search {
    width: 460px;
    margin-right: 80px;
  }

  &__sub-nav {
    a:last-child {
      margin-left: 23px;
    }
    img {
      width: 26px;
      height: 26px;
    }
  }
}
</style>
