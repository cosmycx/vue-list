<template>
  <div class="container">
    <p>Hello Vue</p>

    <SearchBar @termChange="onTermChange"></SearchBar>
    {{ people.length }}

    <PeopleList :people="people"></PeopleList>
  </div>
</template>

<script>
  import axios from 'axios'

  import SearchBar from './components/SearchBar'
  import PeopleList from './components/PeopleList'

  export default {
    name: 'App',
    components: {
      SearchBar,
      PeopleList,
    },
    data() {
      return {
        people: [],
      }
    },
    methods: {
      onTermChange(st) {
        axios.get('https://jsonplaceholder.typicode.com/todos').then(resp => {
          console.log(resp.data)
          this.people = resp.data
        }) // .axios
      }
    }
  }
</script>
