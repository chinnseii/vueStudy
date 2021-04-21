<template>
  <appheader></appheader>
    <div class="about">
    <h1>This is an about page</h1>
  </div>
  
  <appfooter></appfooter>
</template>
<script>
import appfooter from '@/components/Footer.vue'
import appheader from '@/components/Header.vue'
export default {
   components: {
    appfooter,
    appheader
  }
  }
</script>