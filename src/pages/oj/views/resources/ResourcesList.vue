<template>
  <el-row>
  <el-col :span="6" v-for="(o, index) in 3" :key="o" :offset="index > 0 ? 2 : 0">
    <el-card :body-style="{ padding: '0px' }">
      <img src="./python.jpg" class="image">
      <div style="padding: 14px;">
        <span>Python</span>
        <div class="bottom clearfix">
          <el-button type="text" class="button" v-on:click="details">点击学习</el-button>
        </div>
      </div>
    </el-card>
  </el-col>
</el-row>
</template>

<script>
  export default {
    name: 'ResourcesList',
    methods: {
      details () {
        this.$router.push({name: 'resources-details'})
      }
    }
}
</script>

<style scoped lang="less">
.time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
</style>