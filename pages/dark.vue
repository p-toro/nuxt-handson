<template lang="html">
  <div>
    <nuxt-link to="/">TOP</nuxt-link>
    <nuxt-link to="/about">ABOUT</nuxt-link>
    <p class="txt">ダークテーマを適用</p>
  </div>
</template>

<script>
export default {
  layout: 'dark',
  head() {
    return {
      title: 'DARK',
      meta: [
        { hid: 'description', name: 'description', content: 'Dark ページ' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.txt {
  text-align: center;
  color: #ffff00;
}
</style>
