<template>
  <div class="app-container">
    <div class="upload">
      <!-- action是上传的地址可以替换 -->
      <el-upload
        class="upload-demo"
        action="https://jsonplaceholder.typicode.com/posts/"
        :show-file-list="false"
        :on-change="handleChange"
        :file-list="fileList"
      >
        <el-button size="small" type="primary">上传文件</el-button>
        <el-tag type="success">已上传文件数({{ fileList.length }})</el-tag>
      </el-upload>
    </div>
    <el-button
      type="primary"
      plain
      style="position: absolute"
      @click="onSubmit"
    >生成图谱</el-button>

    <el-card class="box-card">
      <img src="@/assets/1.png" width="80%" height="80%">
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fileList: []
    }
  },
  methods: {
    onSubmit() {
      this.$message('生成图谱成功!')
    },
    handleChange(file, fileList) {}
  }
}
</script>

<style scoped>
.line {
  text-align: center;
}
.upload {
  display: inline-block;
  width: 200px;
}
.box-card {
  height: 700px;
  width: 95%;
  margin: 0 auto;
  margin-top: 20px;
}
</style>
