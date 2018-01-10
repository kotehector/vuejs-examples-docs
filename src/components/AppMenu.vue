<template>
  <div class="app-menu">
    <!-- <div ref="logo" class="logo">
      <img 
        @click="toggleCollapse" 
        src="../assets/logo.png">
    </div> -->
    <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
      <el-radio-button :label="false" v-show="isCollapse">
        <div class="logo">
          <img 
            @click="toggleCollapse" 
            src="../assets/logo.png">
        </div>
      </el-radio-button>
      <el-radio-button :label="true" v-show="!isCollapse">
        <div class="logo">
          <img 
            @click="toggleCollapse" 
            src="../assets/logo.png">
        </div>
      </el-radio-button>
    </el-radio-group>
    <el-menu 
      default-active="2" 
      class="el-menu-vertical-demo" 
      @open="handleOpen" 
      @close="handleClose" 
      :collapse="isCollapse">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-menu"></i>
          <span slot="title">Básico</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="1-1">Data Binding</el-menu-item>
          <el-menu-item index="1-2">item two</el-menu-item>
        </el-menu-item-group>
        <!-- <el-menu-item-group title="Group Two">
          <el-menu-item index="1-3">item three</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <span slot="title">item four</span>
          <el-menu-item index="1-4-1">item one</el-menu-item>
        </el-submenu> -->
      </el-submenu>
      <!-- <el-menu-item index="2">
        <i class="el-icon-menu"></i>
        <span slot="title">Navigator Two</span>
      </el-menu-item>
      <el-menu-item index="3">
        <i class="el-icon-setting"></i>
        <span slot="title">Navigator Three</span>
      </el-menu-item> -->
    </el-menu>
  </div>
</template>

<script>
export default {
  name: 'AppMenu',
  data () {
    return {
      isCollapse: true
    }
  },
  methods: {
    toggleCollapse () {
      return this.isCollapse ? 'false' : 'true'
    },
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo {
  border-radius: 50%;
  background-color:#fff;
  height: 50px;
  margin: 25px auto;
  width: 50px;
}
.logo img {
  width: 50%;
  position: relative;
  top: 15px;
}
.el-menu {
  height: calc(100vh - 120px);
}

.el-radio-button {
  border: none;
  padding: 0;
}
</style>
