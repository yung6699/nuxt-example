<template>
  <div>
    <!--    <Header />-->
    <TheHeader @sidenavToggle="displaySidenav = !displaySidenav" />
    <TheSidenav :show="displaySidenav" @close="displaySidenav = false" />
    <Nuxt />
  </div>
</template>
<script>
// import Header from '@/components/Header'
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'
// import TheSideNavToggle from '@/components/Navigation/TheSideNavToggle'

export default {
  components: {
    // Header,
    TheHeader,
    TheSidenav,
  },
  data() {
    return {
      displaySidenav: false,
    }
  },
}
</script>
<style>
body {
  font-family: 'Roboto', 'Open Sans', sans-serif;
}
</style>
