<template>
	<div>
		<div>Login</div>
		<el-input v-model="input" placeholder="请输入内容"></el-input>
		<el-input v-model="input" placeholder="请输入密码" show-password></el-input>
	</div>
</template>

<script>
import Vue from 'vue'
import {Input} from 'element-ui'
Vue.use(Input)
export default {
  name: 'Form'
}
</script>

<style>
</style>
