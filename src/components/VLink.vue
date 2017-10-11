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
  .active {
        width: 130px;
    background: url(/src/imgs/lux_index.png) -8px -215px no-repeat;
    font-size: 14px;
    font-weight: bold;
    height: 38px;
    color: #fff;
    display: inline-block;
    z-index: 999;
  }
  a{
    display: block;
    /* padding: 0px 40px; */
    width: 82px;
    height: 38px;
    color: #c8a985;
  }
  a:hover{
    color: white;
  }
</style>
