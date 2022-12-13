<script>
import AppHeader from './components/AppHeader.vue'
import ListSeries from './components/ListSeries.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: "App",
  components: {
    AppHeader,
    ListSeries,
    AppFooter,
  }
}
</script>

<template>

  <AppHeader />

  <main>

    <ListSeries />

  </main>

  <AppFooter />

</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;
</style>
