<script>
import AppHeader from './components/AppHeader.vue'
import AppIcons from './components/AppIcons.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: "App",
  components: {
    AppHeader,
    AppIcons,
    AppFooter
  }
}
</script>

<template>

  <AppHeader />

  <AppIcons />

  <AppFooter />
  
</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;

</style>
