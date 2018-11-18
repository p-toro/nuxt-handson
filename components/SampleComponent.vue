<template lang="html">
  <div>
    <div class="sample">
      <h1>{{ title }}</h1>
      Hello, I'm {{ name }} {{ reverseName }}
    </div>
    <button
      type="button"
      name="button"
      @click="plus">click times: {{ num }}
    </button>
    <div :class="['hide', { seven: num === 7 }]">
      click 7 times
    </div>
    <div>
      <slot />
    </div>
    <div class="blue">
      <slot name="named" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default Title'
    }
  },
  data() {
    return {
      name: 'p_toro',
      num: 0
    }
  },
  computed: {
    reverseName() {
      return this.name
        .split('')
        .reverse()
        .join('')
    }
  },
  mounted() {
    console.log('mounted')
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;
  &.seven {
    display: block;
  }
}
</style>
