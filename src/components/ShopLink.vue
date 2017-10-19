<template>
  <a 
    v-bind:href="href"
    v-bind:class="{ active: isActive }"
    v-on:click="go"
  >
    <slot></slot>
  </a>
</template>

<script>
  import routes from '../routes'
  import Vue from 'vue'
  import VueRouter from 'vue-router'
  import Detail from '../pages/Detail.vue'
  // const router = new VueRouter({
  //           routes: [
  //             // 动态路径参数 以冒号开头
  //             { path: '/detail/:id', component: Detail, }
  //           ]
  //         })
  export default {
    props: {
      href: {
        type:String,
        required: true 
      }
    },
    computed: {
      isActive () {
        return this.href === this.$root.currentRoute
      }
    },
    methods: {
      go (event) {
        event.preventDefault()
        this.$root.currentRoute = this.href
        window.history.pushState(
          null,
          routes[this.href],
          this.href
        )
      }
    }
  }
</script>

<style scoped>
</style>
