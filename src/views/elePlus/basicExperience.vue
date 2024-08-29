<template>
  <div class="app-container">
    <el-tabs v-model="activeName" class="demo-tabs" @tab-click="handleClick">
      <el-tab-pane label="Button" name="first"></el-tab-pane>
      <el-tab-pane label="Config" name="second">Config</el-tab-pane>
    </el-tabs>
    <div v-if="activeName === 'first'">
      <el-button>Button</el-button>
      <el-button type="primary" icon="CirclePlus">
        Primary Button
      </el-button>
      <el-button type="success" round>Success Button</el-button>
      <el-button type="info">Info Button</el-button>
      <el-button type="primary">
        Upload
      </el-button>
      <el-button type="primary" plain>Text Button</el-button>
      <el-button-group>
        <el-button type="primary" icon="ArrowLeft">Previous Page</el-button>
        <el-button type="primary">
          Next Page<el-icon class="el-icon--right"><ArrowRight /></el-icon>
        </el-button>
      </el-button-group>
    </div>
  </div>

</template>

<script setup>
import { ref } from 'vue'
let activeName = ref('first')
let handleClick = (tab, event) => {
  console.log(tab, event)
}
</script>

<style scoped>

</style>
