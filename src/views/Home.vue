<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="container">
      <n-grid x-gap="12" y-gap="12" cols="4" item-responsive responsive="screen">
        <n-grid-item span="4 m:2 l:1">
          <n-card title="卡片">
            卡片内容
          </n-card>
        </n-grid-item>
        <n-grid-item span="4 m:2 l:1">
          <n-card title="卡片">
            卡片内容
          </n-card>
        </n-grid-item>
      </n-grid>
    </div>
  </div>
</template>

<script setup>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import { 
  NGrid,
  NGridItem,
  NCard
} from 'naive-ui'
</script>

<style lang="scss" scoped>
.container {
  padding: 10px;
}

.n-card-header {
  background-color: #081EA6;
}
</style>