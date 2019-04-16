<template>
  <div>
    <TheHeader />
    <SubMenu />
    <nuxt class="main-content"/>
    <TheHeader />
  </div>
</template>

<script>
import TheHeader from '~/components/TheHeader.vue'
import SubMenu from '~/components/SubMenu.vue'


export default {

  components:{
    TheHeader,
    SubMenu
  }
}
</script>

<style>

*{
  box-sizing: border-box;
}
body{
  font-family: 'Quicksand', sans-serif;
  margin: 0;
}
.main-content{
  margin-top: 5rem;
  margin-bottom: 10rem;
}
</style>




