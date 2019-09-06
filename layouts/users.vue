<template>
  <div>
  <Header />
   <h1>Users layout</h1>
    <nuxt />
  </div>
</template>
<script>
import Header from '@/components/Header.vue'
  export default{
    components: {
      Header
    }
  }
</script>
<style>
  h1{
    color: #3d44ff;
  }

</style>
