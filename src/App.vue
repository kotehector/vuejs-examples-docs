<template>
  <div id="app">
    <el-container>
      <el-header>
        <h1>VueJs Ejemplos Código Documentación</h1>
      </el-header>
      <el-container>
        <el-aside width="200px">
          Barra lateral
          <img src="./assets/logo.png">
        </el-aside>
        <el-container>
          <el-main>
            Principal
            <router-view/>
          </el-main>
        </el-container>
      </el-container>
      <el-footer>
        Pie de página
      </el-footer>
    </el-container>
    
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
