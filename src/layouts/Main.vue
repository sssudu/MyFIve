<template>
  <div>
    <v-head></v-head>
    <v-nav></v-nav>
    <slot></slot>
    <v-footer></v-footer>
    <!-- <v-ad></v-ad> -->
  </div>
</template>

<script>


import VHead from '../components/header.vue'
import VFooter from '../components/Footer.vue'
import VNav from '../components/nav_list.vue'



export default {
  components:{
    VHead,VFooter,VNav
  }
}

</script>

<style scoped>

</style>
