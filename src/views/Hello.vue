<template>
  <div class="">
    <cruddy :columns="columns"
            :resourceURL = "resourceURL"
            width="200"
            height="500"></cruddy>
  </div>
</template>

<script>
import Cruddy from '@/components/Cruddy'

export default {
  name: 'hello',
  components: {
    Cruddy
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      resourceURL: 'https://randomuser.me/api',
      columns: [
        {name: 'title', label: 'Title', field: 'name.title', width: '100', type: 'text', isMandatory: true},
        {name: 'firstName', label: 'First Name', field: 'name.first', width: '200', type: 'text', isMandatory: true},
        {name: 'lastName', label: 'Last Name', field: 'name.last', width: '200', type: 'text', isMandatory: true},
        {name: 'dataOfBirth', label: 'Date of Birth', field: 'dob', type: 'date', width: '200', format: 'yyyy-MM-dd'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
  color: #42b983;
}
</style>
