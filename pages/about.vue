<template lang="html">
  <div>
    <nuxt-link to="/">TOP</nuxt-link>
    <nuxt-link to="/dark">DARK</nuxt-link>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'ABOUT',
      meta: [
        { hid: 'description', name: 'description', content: 'About ページ' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
