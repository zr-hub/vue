<template>
  <el-row class="login-box">
    <el-col :span="8" class="login-box1">
      <p>小U商城管理系统</p>
      <el-form :model="forminfo" ref="form">
        <!-- 账号 -->
        <el-form-item>
          <el-input placeholder="请输入账号" v-model="forminfo.username">
            <template slot="prepend">
              <i class="el-icon-user"></i>
            </template>
          </el-input>
        </el-form-item>
        <!-- 密码 -->
        <el-form-item>
          <el-input placeholder="请输入密码" v-model="forminfo.password">
            <template slot="prepend">
              <i class="el-icon-lock"></i>
            </template>
          </el-input>
        </el-form-item>

        <el-form-item>
          <el-button type="primary" @click="login" class="login-btn">立即创建</el-button>
        </el-form-item>
      </el-form>
    </el-col>
  </el-row>
</template>
<script>
export default {
  data() {
    return {
      forminfo: {
        username: "",
        password: "",
      },
    };
  },
  created() {},
  methods: {
    login() {},
  },
  components: {},
};
</script>
<style scoped>
.login-box {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url("../assets/img/1.jpg");
  background-size: 100% 100%;
}
.login-box1 {
  background-color: #ffffff;
  box-shadow: 0 0 4px 0 rgba(0, 0, 0, 0.3);
  padding: 30px 40px;
  border-radius: 5px;
  border: 1px solid #eeeeee;
}
p {
  line-height: 40px;
  text-align: center;
  margin-bottom: 20px;
}
.login-btn {
  display: block;
  width: 100%;
}
</style>