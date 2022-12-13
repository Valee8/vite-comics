<script>
import AppHeader from './components/AppHeader.vue'
import ListSeries from './components/ListSeries.vue'
import AppIcons from './components/AppIcons.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: "App",
  components: {
    AppHeader,
    ListSeries,
    AppIcons,
    AppFooter,
  }
}
</script>

<template>

  <AppHeader />

  <main>

    <ListSeries />

  </main>

  <AppIcons />

  <AppFooter />

</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;
</style>
