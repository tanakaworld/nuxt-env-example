<template>
  <header class="SharedHeader">
    <ul class="SharedHeader__LinkList">
      <li class="SharedHeader__LinkItem"><nuxt-link
        to="/">Home</nuxt-link></li>
      <li class="SharedHeader__LinkItem"><nuxt-link
        to="/page1">Page1</nuxt-link></li>
      <li class="SharedHeader__LinkItem"><nuxt-link
        to="/page2">Page2</nuxt-link></li>
    </ul>
  </header>
</template>

<style scoped>
.SharedHeader {
  width: 100%;
  height: 40px;
}

.SharedHeader__LinkList,
.SharedHeader__LinkItem {
  margin: 0;
  padding: 0;
}

.SharedHeader__LinkList {
  list-style: none;
  height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.SharedHeader__LinkItem {
  margin-left: 8px;
}
</style>
