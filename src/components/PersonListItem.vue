<template>
  <li class="list-group-item">
    {{ person }}
  </li>
</template>

<script>
  export default {
    name: 'PersonListItem',
    props: {
      person: Object
    }
  }
</script>

<style>
</style>
