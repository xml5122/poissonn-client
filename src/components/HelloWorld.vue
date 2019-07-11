<template>
  <div>
    <el-button type="primary">hello</el-button>
  </div>
</template>
<script>
import Vue from 'vue'
import { Button } from 'element-ui'
Vue.prototype.$ELEMENT = { size: 'small', zIndex: 3000 }
Vue.use(Button)

export default {
  name:"HelloWorld"
}
</script>
<style>
</style>