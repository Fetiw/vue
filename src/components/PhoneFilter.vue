<template>
  <input type="text" v-model="value" @keyup="change">
</template>

<script>
  export default {
    name: 'phone-filter',
    data () {
      return {
        value: ''
      }
    },
    methods: {
      change () {
        this.$emit('filter', this.value)
      }
    }
  }
</script>