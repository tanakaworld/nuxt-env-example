<template>
  <section>
    <h1>Page1</h1>
    <RenderedFrom :render-source="renderSource"/>
    <EnvTable/>
  </section>
</template>

<script>
import EnvTable from '~/components/EnvTable.vue'
import RenderedFrom from '~/components/RenderedFrom.vue'

export default {
  components: {
    EnvTable,
    RenderedFrom
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
