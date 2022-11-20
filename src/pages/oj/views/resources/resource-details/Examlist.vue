<template>
    <el-card class="box-card">
    <div v-for="o in 4" :key="o" class="text item"> 
      {{'考试安排 ' + o }}
    </div>
  </el-card>
</template>

  
  <style>
    .text {
      font-size: 15px;
    }
  
    .item {
      padding: 18px 0;
    }
  
    .box-card {
      width: 480px;
    }
  </style>