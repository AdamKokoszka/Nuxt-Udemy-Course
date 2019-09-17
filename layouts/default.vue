<template>
  <div>
   <TheHeader @sidenavToggle="displaySidenav = !displaySidenav" />
   <TheSidenav :show="displaySidenav" @close="displaySidenav = false" />
    <nuxt />
  </div>
</template>

<style>
  body {
    font-family: 'Open Sans', sans-serif;
    margin: 0;
  }

</style>
<script>
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'
export default{
  components: {
    TheHeader,
    TheSidenav
  },
  data(){
    return{
      displaySidenav: false
    }
  }
}
</script>
