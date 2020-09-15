<template>
  <div>
    <el-button type="primary" @click="add">添加角色</el-button>
    <hr>
    <!-- 列表组件 -->
    <vlist @edit="edit"></vlist>
    <!-- 弹框(添加修改) -->
    <vinfo :info="info" ref="dialog"></vinfo>
  </div>
</template>
<script>
import vinfo from "./vinfo"
import vlist from "./vlist"
export default {
    data(){
        return{ 
          info:{
            isAdd:false,
            isShow:false
          }
         }
    },
    created(){},
    methods:{
      add(){
         this.info.isAdd = this.info.isShow = true
      },
      edit(val){
        this.info.isAdd = false;
        this.info.isShow = true;
        // console.log(val)
        this.$refs.dialog.setinfo(val);//使用setinfo的方法

      }
    },
    components:{
      vlist,vinfo
    }
}
</script>
<style scoped>
</style>