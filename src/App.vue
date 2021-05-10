<template>

  <div id="app">
    <div id="top">
      <el-row>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <router-link to="/login" id="onLogin">请登录</router-link>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light">
            <router-link to="/registers">注册</router-link>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <router-link to="/info">我的资料</router-link>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light">
            <router-link to="/orders">我的订单</router-link>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple">
            <router-link to="/cart">购物车</router-link>
          </div>
        </el-col>
        <el-col :span="4" style="align-content: center">
          <div class="grid-content bg-purple-light" >
            <span v-if="$store.state.isLogin" style="margin: 200px">
        <el-button type="success" round v-on:click="$store.commit('logout')"
        >
          用户已登陆
        </el-button>
      </span>
            <span v-else style="margin: 200px">
      <el-button class="button" type="primary" round v-on:click="$store.commit('login')">登录</el-button>
      </span>
          </div>
        </el-col>
      </el-row>

    </div>
    <div id="nav">
      <el-row :gutter="10">
        <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1">
          <div class="grid-content bg-purple">
            <router-link to="/">主页</router-link>
          </div>
        </el-col>
        <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11">
          <div class="grid-content bg-purple-light">
            <router-link to="/about">关于</router-link>
          </div>
        </el-col>
        <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11">
          <div class="grid-content bg-purple">
            <router-link to="/categories">类别</router-link>
          </div>
        </el-col>
        <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1">
          <div class="grid-content bg-purple-light">
            <router-link to="/cart">购物车</router-link>
          </div>
        </el-col>
      </el-row>

      <router-link to="/details">书籍详情样例</router-link>
    </div>

    <router-view/>

  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

#top a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}

#top a.router-link-exact-active {
  color: #42b983;
}

.el-row {
  margin-bottom: 20px;
}

.el-col {
  border-radius: 4px;
}

.bg-purple-dark {
  background: #99a9bf;
}

.bg-purple {
  background: #d3dce6;
}

.bg-purple-light {
  background: #e5e9f2;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
