<template>

  <div class="Login">
    <div style="margin: 40px">
      please login here
    </div>

    <div style="margin: 20px;"></div>
    <el-form :label-position="labelPosition" label-width="750px" :model="formLabelAlign">
      <el-form-item label="账号" style="text-align: left">
        <el-input v-model="formLabelAlign.name" style="width: 200px"></el-input>
      </el-form-item>
      <el-form-item label="密码" style="text-align: left">
        <el-input v-model="formLabelAlign.region" style="width: 200px"></el-input>
      </el-form-item>
      <el-form-item label="验证码" style="text-align: left">
        <el-input v-model="formLabelAlign.type" style="width: 200px"></el-input>
      </el-form-item>
    </el-form>
    <div>
      <span v-if="$store.state.isLogin" style="margin: 200px">
        <el-button type="warning" round v-on:click="$store.commit('logout')"
        >
          退出登录
        </el-button>
      </span>
      <span v-else style="margin: 200px">
      <el-button class="button" type="primary" round v-on:click="$store.commit('login')">登录</el-button>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      labelPosition: 'right',
      formLabelAlign: {
        name: '',
        region: '',
        type: ''
      }
    };
  }
}
</script>

<style scoped>

</style>