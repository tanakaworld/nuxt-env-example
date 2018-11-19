<template>
  <table>
    <thead>
      <tr>
        <td>Key</td>
        <td>Value</td>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>apiUrl</td>
        <td>{{ apiUrl }}</td>
      </tr>
      <tr>
        <td>API_URL</td>
        <td>{{ API_URL }}</td>
      </tr>
      <tr>
        <td>API_URL_FROM_NUXT_ENV</td>
        <td>{{ API_URL_FROM_NUXT_ENV }}</td>
      </tr>
      <tr>
        <td>notDefined</td>
        <td>{{ notDefined }}</td>
      </tr>
      <tr>
        <td>NOT_DEFINED</td>
        <td>{{ NOT_DEFINED }}</td>
      </tr>
      <tr>
        <td>SENTRY_DSN</td>
        <td>{{ SENTRY_DSN }}</td>
      </tr>
      <tr>
        <td>SENTRY_DSN_FROM_NUXT_ENV</td>
        <td>{{ SENTRY_DSN_FROM_NUXT_ENV }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: 'EnvTable',
  data() {
    return {
      apiUrl: process.env.apiUrl,
      API_URL: process.env.API_URL,
      API_URL_FROM_NUXT_ENV: this.$env.API_URL,
      notDefined: process.env.notDefined,
      NOT_DEFINED: process.env.NOT_DEFINED,
      SENTRY_DSN: process.env.SENTRY_DSN,
      SENTRY_DSN_FROM_NUXT_ENV: this.$env.SENTRY_DSN
    }
  }
}
</script>

<style scoped>
table {
  border-collapse: collapse;
}

table,
th,
td {
  border: 1px solid black;
}

td {
  padding: 16px;
}
</style>
