<template>
  <div class="hello">
    <el-row>
      <el-col :span="4">
        <div class="sidebar">
          <div class="logo">
            <img src="../../static/images/logo.png" alt="">
          </div>
          <div class="robot-admin">
            <el-tree :data="data" :highlight-current="true" @node-click="toggle"></el-tree>
          </div>
        </div>
      </el-col>
      <el-col :span="20">
        <div class="main">
          <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" active-text-color="#2781EE">
            <el-menu-item index="1">一个菜单</el-menu-item>
            <el-menu-item index="2">两个菜单</el-menu-item>
            <el-menu-item index="3">三个菜单</el-menu-item>
          </el-menu>
          <div class="view">
            <Test></Test>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import Test from './Test'
export default {
  name: "HelloWorld",
  components:{
    Test
  },
  data() {
    return {
      data: [
        {
          label: '采集机器人',
          children: [{
            label: '采集机器人管理'
          }]
        }
      ],
      activeIndex:"1"      
    }
  },
  methods: {
    toggle(data) {
      console.log(data);
    }
  }
};
</script>

<style scoped>
.hello{
  height:100%;
  min-height:800px;
}
.el-row{
  height:100%;
}
.el-col{
  height:100%;
}
.sidebar{
  height:100%;
  background-color: RGB(238, 238, 238);
}
.main{
  height:100%;
}
.logo{
  width:60%;
  min-height:40px;
  margin:0 auto;
  padding-top:50px;
}
.logo img{
  width:100%;
  height:100%;
}
.el-tree{
  margin:50px auto 0;
}
.el-menu{
  display: flex;
  justify-content: center;
  background-color:RGB(238, 238, 238);
}

</style>
