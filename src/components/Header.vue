<template>
  <el-header>
<div id="nav">
<el-row :gutter="10">
    <el-col :span="5">
      <div class="grid-content bg-purple">
        <router-link to="/"><a>サイト名</a></router-link>
        
      </div>
    </el-col>
     <el-col :span="9">

</el-col>
  <el-col :span="5">
    <div class="grid-content bg-purple">
<router-link to="/login">ログイン</router-link>
    </div>
</el-col>
  <el-col :span="5">
    <div class="grid-content bg-purple">
      <router-link to="/about">新規登録</router-link> 
    </div>     
</el-col>
  </el-row>
</div>
      </el-header>
</template>
<style lang="scss">
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
#nav {
  a ,p{
    text-decoration: none;
    font-weight: bold;
    color: #a7b1b9;
    &.router-link-exact-active {
      color: #6cbd2a;
    }
  }
}
  .el-row {
    margin-bottom: 10px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>
