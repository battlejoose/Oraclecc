<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<script>
export default {
  name: 'App',
  created () {
    this.$q.dark.set(true)
    // colors.setBrand('light', '#DDD')
    // colors.setBrand('primary', '#263f10')
    // colors.setBrand('primary', '#F33', document.getElementById('rebranded-section-id'))
  }
}
</script>
