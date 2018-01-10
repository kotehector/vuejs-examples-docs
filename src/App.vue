<template>
  <div id="app">
    <el-container>
      <el-header>
        <h1>VueJs Ejemplos Código Documentación</h1>
      </el-header>
      <el-container>
        
        <app-menu></app-menu>
        
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
import AppMenu from '@/components/AppMenu'
export default {
  name: 'app',
  components: {
    AppMenu
  }
}
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.el-header,
.el-footer {
  background-color: #64b587;
  color: #fff;
}
.el-footer {
  position: fixed;
  bottom: 0;
  width: 100%;
}
</style>
