<template>
  <router-view></router-view>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      res:{}
    }
  },
  mounted(){
    // 本地加载请求静态json文件的形式
    this.axios.get('/user/login').then((res)=>{
      this.res = res;
    });
  }
}
</script>

<style lang="scss">

</style>

