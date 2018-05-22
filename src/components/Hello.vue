<template>
  <div class="hello">
    <h1>{{ todos }}</h1>
    <button @click="test">Add</button>
  </div>
</template>

<script>
  import db from '../graphql'

  export default {
    name: 'hello',
    data () {
      return {
        todos: db.todos
      }
    },
    methods: {
      test () {
        db.todos.push({
          test: 'test'
        })
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #35495E;
  }
</style>
