<!-- 准备些 cnodejs 的列表页面 -->
<template>
<div>
  index page
</div>
</template>

<script>
// nodejs的信息 可以在浏览器调试下console看到
export default {
  created() {
    this.$api.get('topics', null, r => {
      console.log(r)
    })
  }
}
</script>
