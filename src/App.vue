<template>
 <div id="app">
   <!-- 顶级路由 -->
   <router-view></router-view>
 </div>
</template>
<script>
export default {
 name:"App",
 data(){
 return{}
 },
 created(){},
 methods:{},
 components:{}
}

</script>
<style>
*{padding: 0;margin: 0;}
.toggle-btn{
  font-size: 14px;
}
.table-bg{
  background-color: #ffffff;
  padding: 20px;
  margin: 15px 0;
}
.el-dialog__header{
  border: 1px solid #dddddd;
  padding: 15px 20px 10px!important;
}
</style>