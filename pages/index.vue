<template>
  <section>
    <h1>Home</h1>
    <RenderedFrom :render-source="renderSource"/>
    <EnvTable/>
  </section>
</template>

<script>
import EnvTable from '~/components/EnvTable.vue'
import RenderedFrom from '../components/RenderedFrom'

export default {
  components: {
    RenderedFrom,
    EnvTable
  },
  asyncData() {
    return {
      renderSource: process.static
        ? 'static'
        : process.server
          ? 'server'
          : 'client'
    }
  }
}
</script>
