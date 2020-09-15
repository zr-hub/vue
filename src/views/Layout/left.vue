<template>
  <div>
    <h3 class="logo">小U商城后台</h3>
    <!-- 菜单组件 -->
    <el-menu class="pages-menu" text-color="#fff" background-color="#444" router :default-active="$route.path" :collapse="iscollapse">
      <!-- <el-submenu index="/index">
        <template slot="title" index="1">
          <i class="el-icon-house"></i>
          <span>后台首页</span>
        </template>
      </el-submenu> -->
      <el-menu-item index="/index"><i class="el-icon-house"></i><span slot="title">后台首页</span></el-menu-item>
      <el-submenu index="2">
        <template slot="title">
          <i class="el-icon-setting"></i>
          <span>系统设置</span>
        </template>
        <el-menu-item index="/menu">菜单管理</el-menu-item>
        <el-menu-item index="/role">角色管理</el-menu-item>
        <el-menu-item index="/user">管理员管理</el-menu-item>
      </el-submenu>
      <el-submenu index="3">
        <template slot="title">
          <i class="el-icon-menu"></i>
          <span>商城管理</span>
        </template>
        <el-menu-item index="3-1">分类管理</el-menu-item>
        <el-menu-item index="3-2">规格管理</el-menu-item>
        <el-menu-item index="3-3">商品管理</el-menu-item>
        <el-menu-item index="3-4">会员管理</el-menu-item>
        <el-menu-item index="3-5">轮播图管理</el-menu-item>
        <el-menu-item index="3-6">秒杀管理</el-menu-item>
      </el-submenu>
    </el-menu>
  </div>
</template>
<script>
import {mapState} from 'vuex'
export default {
  data() {
    return {};
  },
  computed:{
    ...mapState(['iscollapse'])
  },
  created() {},
  methods: {},
  components: {},
};
</script>
<style scoped>
.logo {
  line-height: 60px;
  color: #fff;
  background-color: #666;
  text-align: center;
  white-space: nowrap;
  overflow: hidden;
}
.pages-menu{
    border-right: none;
}
</style>