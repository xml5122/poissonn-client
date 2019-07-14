<template>
  <div>
  	<el-container>
	  <el-header><index-header></index-header></el-header>
	  <el-container>
	    <el-aside width="200px"><index-navigat></index-navigat></el-aside>
	    <el-container>
	      <el-main><index-main></index-main></el-main>
	      <el-footer><index-foot></index-foot></el-footer>
	    </el-container>
	  </el-container>
	</el-container>
    
    
    
    
  </div>
</template>

<script>
import IndexHeader from './components/Header'
import IndexNavigat from './components/Navigat'
import IndexMain from './components/Main'
import IndexFoot from './components/Foot'
export default {
  name: 'Index',
  components:{ IndexHeader, IndexNavigat, IndexMain, IndexFoot}
}
</script>

<style>
</style>
