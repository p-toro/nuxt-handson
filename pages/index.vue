<template>
  <section>
    <nuxt-link to="/about">ABOUT</nuxt-link>
    <nuxt-link to="/dark">DARK</nuxt-link>
    <sample-component :title="title">
      Hello Slot!
      <div slot="named">
        named slot
      </div>
    </sample-component>
  </section>
</template>

<script>
import SampleComponent from '~/components/SampleComponent.vue'

export default {
  components: {
    SampleComponent
  },
  data() {
    return {
      title: 'Nuxt.js Handson!'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
