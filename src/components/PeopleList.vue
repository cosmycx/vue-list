<template>
  <ul class="list-group">
    <PersonListItem
      v-for="person in people"
      :person="person"
      :key="person.id"
      >
    </PersonListItem>
  </ul>
</template>

<script>
  import PersonListItem from './PersonListItem'
  export default {
    name: 'PeopleList',
    components: {
      PersonListItem,
    },
    props: {
      people: Array
    },
  }
</script>

<style>
</style>
