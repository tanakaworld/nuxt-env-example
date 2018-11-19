<template>
  <div class="RenderedFrom">Rendered From:{{ renderSource }}</div>
</template>

<script>
export default {
  props: {
    renderSource: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.RenderedFrom {
  margin: 16px 0;
}
</style>
