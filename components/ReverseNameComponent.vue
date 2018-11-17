<template lang="html">
  <div class="sample">
    Hello, I'm {{ name }} {{ reverseName }}
  </div>
</template>
​
<script>
export default {
  data() {
    return {
      name: 'SSSS:GRIDMAN'
    }
  },
  computed: {
    reverseName() {
      return this.name
        .split('')
        .reverse()
        .join('')
    }
  }
}
</script>
