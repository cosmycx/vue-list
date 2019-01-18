<template>
  <div>
    <input @input="onInput"/>
  </div>

</template>

<script>

  export default {
    name: 'SearchBar',
    methods: {
      onInput(ev) {
        this.$emit('termChange', ev.target.value)
      }
    },
  }

</script>

<style scoped>
  input {
    width: 75%;
  }
  div {
    margin: 20px;
    text-align: center;
  }

</style>
