<template>
  <el-row class="container">
    <!--头部-->
    <!-- <el-col :span="24"><router-view name="top"></router-view></el-col> -->
    <el-col :span="24" class="main" style="top: 0px">
      <!--左侧导航-->
      <router-view name="aside"></router-view>
      <!--右侧内容区-->
      <section class="content-container">
        <div class="grid-content bg-purple-light">
          <el-col :span="24" class="content-wrapper">
            <transition name="fade" mode="out-in">
              <router-view></router-view>
            </transition>
          </el-col>
        </div>
      </section>
    </el-col>
  </el-row>
</template>
<script>
  export default {
    name: 'home',
    data () {
      return {
        loading: true
      }
    }
  }
</script>
<style>
  .container .main {
      top: 0px;
  }
</style>
