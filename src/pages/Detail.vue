<template>
  <main-layout>
    <v-detail-title></v-detail-title>
  </main-layout>
</template>
<script>
import routes from '../routes.js'
import MainLayout from '../layouts/Main.vue'
import VueRouter from 'vue-router'
import VDetailTitle from '../components/DetailTitle.vue'
export default {
  props:['id'],
  components:{
      MainLayout,VDetailTitle
  }
}
</script>
<style>
@import   '/static/common/common.css';
*{
  margin: 0;
  padding: 0;
  }
</style>
