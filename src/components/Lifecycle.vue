<template>
<div>VISIBLE LIFECYCLE {{ adrien }}</div>
</template>

<script>
export default {
  name: 'Lifecycle',
  props: {
    adrien: {
      type: String,
      required: true,
    },
  },
  watch: {
    adrien(newVal, oldVal) {
      console.log('ancienne', oldVal)
      console.log('nouvelle', newVal)
    }
  },
}
</script>