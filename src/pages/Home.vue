<template>
  <div>
    <main-layout>
      
      <v-swiper></v-swiper>
      <v-body >
        
      </v-body>
    </main-layout>
    
    <ad-fixed></ad-fixed>
  </div>
  
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import AdFixed from '../components/AdFixed.vue'
  import VSwiper from '../components/Swiper.vue'
  import VBody from '../layouts/Home_body.vue'
  export default {
    components: {
      MainLayout,AdFixed,VSwiper,VBody
    }
  }
</script>
<style>
  @import   '/static/common/common.css';
  *{
  margin: 0;
  padding: 0;
  }
body{
  font: 12px/200% 'microsoft yahei','微软雅黑',Helvetica,Arial,Tahoma,"黑体",'宋体',sans-serif;
}
</style>

