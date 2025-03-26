<template>
  <el-container>
    <el-header>
      <el-menu class="navigation" :default-active="activeLink">
        <h1>My Portfolio</h1>

        <div>
          <router-link to="/">
            <el-menu-item index="/">Home</el-menu-item>
          </router-link>
          <router-link to="/">
            <el-menu-item index="2">About Me</el-menu-item>
          </router-link>
          <!-- <router-link to="/">
            <el-menu-item index="3">Hire Me</el-menu-item>
          </router-link> -->
        </div>
      </el-menu></el-header
    >
    <el-main> <RouterView /></el-main>
  </el-container>
</template>

<script lang="ts">
export default {
  data() {
    return {
      activeLink: '',
    }
  },
  mounted() {
    this.activeLink = this.$route.path
  },
}
</script>

<style scoped>
.navigation {
  width: 100%;
  display: flex;
  justify-content: space-between;
  position: relative;
  border-radius: 5px;
  text-align: center;
}

.navigation h1 {
  font-size: 30px;
  margin: 20px;
  color: var(--el-menu-text-color);
}

.navigation div {
  display: flex;
  justify-content: space-around;
  border: 1px solid;
  width: 80%;
}

.navigation div a li {
  height: 100%;
  font-size: 16px;
}

.el-menu-item {
}
</style>
