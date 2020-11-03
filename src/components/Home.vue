<template>
  <div>
    <el-button type="info" @click="logout">退出</el-button>
  </div>
</template>

<script>
export default {
  methods: {
    // 退出
    logout() {
      // 1.清空token
      window.sessionStorage.removeItem('token')
      // 2.提示
      this.$message.success('退出成功')
      // 3.跳转到登录页
      this.$router.push('/login')
    }
  }
}
</script>

<style></style>
