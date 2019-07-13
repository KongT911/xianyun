<template>
  <div class="header">
    <el-row type="flex" class="main" justify="space-between">
      <!-- 这是log -->
      <div class="log">
        <nuxt-link to="/">
          <img src="http://157.122.54.189:9093/images/logo.jpg" alt />
        </nuxt-link>
      </div>
      <!-- 导航栏 -->
      <el-row type="flex" class="navigationBar">
        <nuxt-link to="/">首页</nuxt-link>
        <nuxt-link to="/post">旅游攻略</nuxt-link>
        <nuxt-link to="/hotel">酒店</nuxt-link>
        <nuxt-link to="/air">国内机票</nuxt-link>
      </el-row>
      <!-- 用户名 -->
      <div class="headerRight">
        <div>
          <nuxt-link to="/user/login" v-if="false">登录注册</nuxt-link>
        </div>
        <div>
          <el-dropdown>
            <span class="el-dropdown-link">
              <img src="http://157.122.54.189:9095/assets/images/avatar.jpg" alt />
              旧习难改
              <i class="el-icon-arrow-down el-icon--right"></i>
            </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>个人中心</el-dropdown-item>
              <el-dropdown-item>退出</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>
      </div>
    </el-row>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.header {
  box-shadow: 0 2px 2px #ddd;
  .main {
    width: 1000px;
    margin: 0 auto;
    height: 60px;
    line-height: 60px;
    align-items:center;
  }
  .log {
    width: 156px;
    height: 43px;
    margin-right: 20px;
    img {
      width: 100%;
    }
  }
  .navigationBar {
    flex: 1;
    a {
      display: block;
      height: 60px;
      padding: 0 20px;
      box-sizing: border-box;
      &:hover{
        color:#409eff;
        border-bottom: 5px solid #409eff;
      }
    }
    .nuxt-link-exact-active{
      background-color: #409eff;
      &:hover{
        color:#fff;
      }
    }
  }
  .headerRight {
    img {
      width: 36px;
      height: 36px;
      vertical-align: middle;
    }
  }
}
</style>

