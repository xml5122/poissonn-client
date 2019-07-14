<template>
	<el-form ref="login" :model="login" :rules="rules" label-width="80px" class="el-loginForm">
	  <el-form-item label="账号" prop="username">
	    <el-input v-model="login.username"></el-input>
	  </el-form-item>
	  <el-form-item label="密码" prop="password">
	    <el-input v-model="login.password" show-password></el-input>
	  </el-form-item>
    <router-link to='/index'>
  	  <el-form-item>
  	    <el-button type="primary" @click="onSubmit('login')">登录</el-button>
  	  </el-form-item>
    </router-link>
	</el-form>
</template>

<script>
import https from '@/https'
export default {
  name: 'Form',
   data() {
      return {
        login: {
          username: '',
          password: ''
        },
        rules: {
          username: [
            { required: true, message: '账号不能为空',trigger: 'blur' }
          ],
          password: [
            { required: true, message: '密码不能为空',trigger: 'blur' }
          ]
        }
      }
    },
    methods: {
      onSubmit(formName) {
      	let params ={'username': this.login.username, 'password': this.login.password}
      	https.fetchPost('/user/login',params ).then((data) => {
            //this.base.token = data.data.token　　　　
            //console.log("this.base.tokenthis.base.token",this.base.token)
            alert(data);

        }).catch(err=>{
                console.log(err)
         }
        )
      }
  	}
}
</script>

<style lang="stylus" scoped>
  .el-loginForm
    position: absolute
    opacity: 0.6
    width: 20%
    padding-top: 30%
    padding-left: 40%
    text-align: center
</style>
