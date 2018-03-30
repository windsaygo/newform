
<template>
  


<el-container style="height: 300px; border: 1px solid #eee">
  <el-aside width="200px" style="background-color: rgb(238, 241, 246)">
    <el-menu :default-openeds="['2', '3']">  
      <el-submenu index="2">
        <template slot="title"><i class="el-icon-menu"></i>产品分类</template>
        <el-menu-item-group>
          <template slot="title">智能家居</template>
          <el-menu-item index="2-1">智能家电</el-menu-item>
          <el-menu-item index="2-2">数码产品</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="电子产品">
          <el-menu-item index="2-3">苹果系列</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="2-4">
          <template slot="title">其它</template>
          <el-menu-item index="2-4-1">边缘产品</el-menu-item>
        </el-submenu>
      </el-submenu>  
    </el-menu>
  </el-aside>
  <el-container>


    <el-header style="text-align: right; font-size: 12px">
      <el-dropdown>
        <i class="el-icon-setting" style="margin-right: 15px"></i>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>查看</el-dropdown-item>
          <el-dropdown-item>新增</el-dropdown-item>
          <el-dropdown-item>删除</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <span>windsaygo</span>
    </el-header>
    
    <el-main>
      <el-table :data="tableData">
        <el-table-column prop="date" label="产品名称" width="120">
        </el-table-column>
        <el-table-column prop="name" label="规格型号" width="120">
        </el-table-column>
        <el-table-column prop="address" label="货存数量" width="120">
        </el-table-column>
      </el-table>
    </el-main>
  </el-container>
</el-container>
</template>
<style>
  .el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
  }
  
  .el-aside {
    color: #333;
  }
</style>

<script>
  export default {
    data() {
      const item = {
        date: '平板遥控电视',
        name: 'TCL',
        address: '17'
      };
      return {
        tableData: Array(10).fill(item)
      }
    }
  };
</script>