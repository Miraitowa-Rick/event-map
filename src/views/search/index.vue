<template>
  <div class="app-container">
    <el-input
      v-model="input"
      placeholder="请输入搜索内容"
      clearable
      style="width: 150px; margin-right: 30px"
    />
    <el-button type="primary" plain>搜索</el-button>
    <el-card class="box-card">
      <img src="@/assets/2.png" width="80%" height="80%">
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: ''
    }
  },
  methods: {
    onSubmit() {
      this.$message('submit!')
    },
    onCancel() {
      this.$message({
        message: 'cancel!',
        type: 'warning'
      })
    }
  }
}
</script>

<style scoped>
.line {
  text-align: center;
}
.box-card {
  height: 700px;
  width: 95%;
  margin: 0 auto;
  margin-top: 20px;
}
</style>
