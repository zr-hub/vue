<template> 
<el-container class="page">
    <el-aside width="iscollapse ? '18px':'200px'" class="page-nav">
        <left></left>
    </el-aside>
    <el-container class="page-content">
        <el-header class="page-header">
            <top></top>
        </el-header>
        <el-main height="" class="page-main"> 
            <router-view/>
        </el-main>
    </el-container>
</el-container>
</template>
<script>

import left from './left'
import top from './top'
import { mapState} from 'vuex'

export default {
    data(){
        return{  }
    },
    computed:{
        ...mapState(['iscollapse'])
    },
    created(){},
    methods:{},
    components:{
        left,top
    }
}
</script>
<style scoped>
.page{
    width: 100vw;
    height: 100vh;
}
.page-nav{
    height: 100%;
    background-color: #444;
}
.page-content{
    height: 100%;
    background-color: #f7f7f7;
}
.page-header{
    background-color: #ffffff;
    box-shadow:  0 0 4px 0 rgba(0,0,0,.3);
}
</style>