<template>
  <section style="flex: 1">
    <el-card>
      <div slot="header" class="cleafix">
        <span>ログイン</span>
      </div>
      <form>
        <div class="form-content">
          <span>ユーザーID</span>
          <el-input placeholder="" v-model="formData.id" />
        </div>
        <div class="form-content">
          <el-checkbox v-model="isCreateMode">アカウントを作成する</el-checkbox>
        </div>
        <div class="text-right">
          <el-button type>{{buttonText}}</el-button>
        </div>
      </form>
    </el-card>
  </section>
</template>


<script>
export default {
  asyncData() {
    return {
      isCreateMode: false,
      formData: {
        id: ''
      }
    }
  },
  computed: {
    buttonText() {
      return this.isCreateMode ? '新規登録' : 'ログイン'
    }
  }
}
</script>

<style>
.form-content {
  margin: 16px 0;
}
</style>
