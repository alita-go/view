<template>
  <div>
    _id.vue
  </div>
</template>

<script>
  export default {
    asyncData({isDev, route, store, env, params, query, req, res, redirect, error}) {
      console.log(route);
    },
  }
</script>

<style lang="less" scoped>
  
</style>
