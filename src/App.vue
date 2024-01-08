<script>

import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import AppMain from './components/AppMain.vue'

export default {
  components: [
    AppHeader,
    AppFooter,
    AppMain,
  ],
}

</script>

<template>
  <div>
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>
</template>

<style lang="scss">
@use './styles/general.scss'
</style>