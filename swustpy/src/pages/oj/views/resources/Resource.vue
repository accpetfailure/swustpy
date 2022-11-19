
<template>
  <div class="Resource">
    <el-container>
      <el-header><div><h1 class="title">python1</h1></div>
        <!-- <el-button type="danger">登录</el-button> -->
      </el-header>
      <el-container>
        <el-aside class="commonaside" width="200px">
          <el-menu background-color="#CAE1FF" text-color="black"  :default-active="this/$route.path" router= "true">
            <el-menu-item index="/resources/:resourceID/announce">
              <template #title>
                <i class="el-icon-postcard"></i>
                <span>公告</span>
              </template>
            </el-menu-item>
            <el-menu-item index="/resources/:resourceID/content">
              <template #title><i class="el-icon-document-copy"></i>
                <span>课件</span>
              </template>
            </el-menu-item>
            <el-menu-item index="/resources/:resourceID/testlist">
              <template #title>
                <i class="el-icon-notebook-2"></i>
                <span>测试</span>
              </template>
            </el-menu-item>
            <!-- </el-submenu>  -->
            <el-submenu index="1">
              <template #title>
                <i class="el-icon-set-up"></i>
                <span>考试</span>
              </template>
               <el-menu-item-group>
                <el-menu-item index="/resources/:resourceID/examlist">考试安排</el-menu-item>
              </el-menu-item-group> 
            </el-submenu>
            <el-menu-item index="/resources/:resourceID/forumindex">
              <template #title>
                <i class="el-icon-chat-line-round"></i>
                <span>讨论区</span>
              </template>
            </el-menu-item>
          </el-menu>
        </el-aside>
        <el-main>
          <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'Resource'
}
</script>

<style>
.el-container {
  height: 100vh;
}
.el-header{
  background-color:#CAE1FF;
  /* text-align:left; */
}
.commonaside {
  background: #CAE1FF;
}
</style>


