<template>
<div>
  <img src="../../src/assets/logo.png"> 
  <el-button @click="visible=true">点击登陆</el-button>
  <el-dialog :visible.sync="visible" title="登陆">
    <el-form ref="loginForm" :model="loginForm" :rules="rules" label-width="120px">
      <el-form-item label="用户名" prop="name">
        <el-input v-model="loginForm.name" placeholder="请输入用户名"></el-input>
      </el-form-item>
      <el-form-item label="密码" prop="password">
        <el-input v-model="loginForm.password" placeholder="请输入密码"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="submit('loginForm')">登陆</el-button>
        <el-button @click="resetForm('loginForm')">重置</el-button>
      </el-form-item>
    </el-form> 
  </el-dialog>
</div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      visible: false,
      loginForm:{
        name: "",
        password: ""
      },
      rules: {
        name: [
          { required: true, message: '请输入用户名！', trigger: 'blur' },
        ],
        password: [
          { required: true,  message: '请输入密码！', trigger: 'blur' },
          { min: 5, max:10, message: '密码长度在 5 到 10 个字符！', trigger: 'blur'}
        ]
      }
    };
  },
  methods: {
    submit(formName) {
      this.$refs[formName].validate((valid) => {
        if(valid) {
          alert(111)
          window.location.href = "/Main"
          this.$refs[formName].resetFields();
        }
      })
    },
    resetForm(formName) {
        this.$refs[formName].resetFields();
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
