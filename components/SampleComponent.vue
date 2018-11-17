<template lang="html">
  <div class="sample">
    <h1>{{ title }}</h1>
    Hello, I'm {{ name }}
    <div>
      <slot/>
    </div>
    <div class="blue">
      <slot name="named"/>
    </div>
  </div>
</template>
​
<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Defalut Title'
    }
  },
  data() {
    return {
      name: 'o1ive参上！！'
    }
  }
}
</script>
