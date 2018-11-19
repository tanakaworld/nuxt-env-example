<template>
  <section>
    <h1>Page2</h1>
    <RenderedFrom :render-source="renderSource"/>
    <EnvTable/>
    {{ name }}
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
  },
  data() {
    const name = this.user.name
    return { name }
  }
}
</script>
