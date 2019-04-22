<template>
  <div>
    <TheHeader />
    <nuxt class="main-content"/>
    <subFooter />
    <TheFooter />
  </div>
</template>

<script>

import TheHeader from '~/components/TheHeader.vue'
import subFooter from '~/components/subFooter.vue'
import TheFooter from '~/components/TheFooter.vue'

export default {

  components:{
    TheHeader,
    subFooter,
    TheFooter
  }
}
</script>

<style>

*{
  box-sizing: border-box;
}
body{
  font-family: 'Quicksand', sans-serif;
  /*margin: 0; */
  height: 100%;
}
.main-content{

  margin-top: 5rem;
  margin-bottom: 10rem;
}
</style>




