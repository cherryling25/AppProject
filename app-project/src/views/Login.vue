<template>
<div id="login-container">

  <div class="logo">
    <img src="../assets/login-logo.jpg" width="350px" height="350px">
  </div>
  
  <form class="formcontent">
  <div class="form-group">
    <i class="glyphicon glyphicon-user"></i>
    <label for="inputtext">用户名</label>
    <input type="text" class="form-control" id="inputtext" placeholder="请输入用户名">
  </div>
  <br>
  
  <div class="form-group">
    <label for="inputpassword">密码&nbsp;&nbsp;&nbsp;&nbsp;</label>
    <input type="password" class="form-control" id="inputpassword" placeholder="请输入密码">
  </div>

  <br>
  <button type="submit" class="btn btn-default btn-group-lg">登陆</button>

    <p>没有账户？ <a href="">注册</a></p>
  
</form>
</div>
</template>



<script>
$(function(){
  alert(1);
});
export default {
  name : 'login',
  /* data() {
      return {
        ruleForm: {
          account: 'admin',
          checkPass: '12345'
        },
        rules: {
          account: [
            { required: true, message: '请输入账号', trigger: 'blur' },
          ],
          checkPass: [
            { required: true, message: '请输入密码', trigger: 'blur' },
          ]
        },
        checked: true
      };
    },
  methods:{
    resetForm(formName) {
        this.$refs['ruleForm'].resetFields();
    },
     handleSubmit(ev) {
        var _this = this;
        this.$refs.ruleForm.validate((valid) => {
          if (valid) {

            var loginParams = { accountName: this.ruleForm.account, inputedPassword: this.ruleForm.checkPass };
            requestLogin(loginParams).then(data => {
              if (!data) {
                this.$message({
                  message: 'Incorrect userName or password',
                  type: 'error'
                });
              } else {
                this.$router.push({ path: '/productinfo' });
              }
            });
           
          } else {
            console.log('error submit!!');
            return false;
          }
        });
      }

  } */
}
</script>

<style scoped>
#login-container {
    border-radius: 5px;
    background-clip: padding-box;
    margin: 20px auto;
    width: 350px;
    
    background: #fff;
    border: 1px solid #eaeaea;
    box-shadow: 0 0 25px #cac6c6;
  }

.formcontent{
  margin-left: 25px;
  margin-top:25px;
}

input{
  border:none;
  border-bottom:1px solid black;
  background:transparent;
  margin-left: 8px;
  size: 20px;
  width: 75%;
  height: 10px;
   padding: 10px 0px;
  outline: none;
  font-size: 15px;
}

::-webkit-input-placeholder {
     color: gray;
     font-size: 15px;
     padding-left: 10px;
   
 }



button{
  margin-top: 10px;

}
</style>
