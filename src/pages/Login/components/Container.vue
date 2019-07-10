<template>
    <el-container>
	  <el-header>Poisson管理后台</el-header>
	  <el-main><login-form></login-form></el-main>
	  <el-footer>{{this.date}}</el-footer>
	</el-container>
</template>
<script>
import LoginForm from './Form'
export default {
  name: 'Container',
  data () {
      return {
      date:new Date()
    }
  },
  components: {LoginForm}
}
</script>
<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .el-container
    height: 100%
    margin: 0
    padding: 0
    overflow: hidden
    .el-header
      background-color: $bgColor
      color: $borderColor
      text-align: center
      position: absolute
      top: 0
      width: 100%
      padding-top: 20px
      font-size: 20px
      font-weight: bold
      letter-spacing: 3px
    .el-footer
      background-color: $bgColor
      color: #fff
      text-align: center
      position: absolute
      bottom: 0
      width: 100%;
      padding-top: 20px
    .el-main
      background-color: #fff
      color: $borderColor
      text-align: center
      height: 100%
      margin: 0
      overflow: hidden
      top: 60px
      bottom: 60px
      position: fixed
      width: 100%
</style>