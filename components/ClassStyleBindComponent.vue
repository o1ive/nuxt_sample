<template lang="html">
  <div class="sample">
    <div>
      <button
        type="button"
        name="button"
        @click="plus">click times: {{ num }}</button>
    </div>
    <div :class="['hide', { seven: num === 7 }]">
      click 7 times
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0
    }
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
