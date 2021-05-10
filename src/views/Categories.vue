<template>
  <div class="categories">
    <div>
      <div class="line"></div>
      <el-menu
          :default-active="activeIndex2"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#545c64"
          text-color="#fff"
          active-text-color="#ffd04b">
        <el-menu-item index="1">类别</el-menu-item>
        <el-submenu index="2">
          <template #title>书目</template>
          <el-menu-item index="2-1">小说</el-menu-item>
          <el-menu-item index="2-2">艺术</el-menu-item>
          <el-menu-item index="2-3">教育</el-menu-item>
          <el-submenu index="2-4">
            <template #title>人文社科</template>
            <el-menu-item index="2-4-1">历史</el-menu-item>
            <el-menu-item index="2-4-2">政治/军事</el-menu-item>
            <el-menu-item index="2-4-3">法律/政治</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-menu-item index="3" disabled>消息中心</el-menu-item>
        <el-menu-item index="4"><a href="Orders.vue" target="_blank">订单管理</a></el-menu-item>
        <el-menu-item index="5"><a href="Cart.vue" target="_blank">购物车</a></el-menu-item>
      </el-menu>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style scoped>

</style>