<template>
  <button @click="toto">{{ label }}</button>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    label: {
      type: String,
      required: true,
    }
  },
  methods: {
    toto() {
      this.$emit('tutu')
    }
  }
}
</script>