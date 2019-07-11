<template>
    <el-container>
    <el-main>
      <img :src="bg" class="el-img" />
      <login-form></login-form>
    </el-main>
    <el-footer>{{this.date}}</el-footer>
  </el-container>
</template>
<script>
import LoginForm from './Form'
export default {
  name: 'Container',
  data () {
      return {
      date:new Date(),
      bg: require('photo/timg.jpg'),
    }
  },
  components: { LoginForm}
}
</script>
<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .el-container
    height: 100%
    margin: 0
    padding: 0
    overflow: hidden
    .el-footer
      background-color: $bgColor
      color: #fff
      text-align: center
      position: absolute
      bottom: 0
      width: 100%;
      padding-top: 20px
    .el-main
      position: absolute
      height: 100%
      width: 100%
      padding: 0
    .el-img
      position: absolute
      height: 100%
      width: 100%
</style>