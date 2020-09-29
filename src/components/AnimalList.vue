<template>
  <div class="hello">
    <table>
      <thead>
        <tr>
          <th>sort</th>
          <th>name</th>
          <th>date of birth</th>
        </tr>

      </thead>
      <tbody>
        <tr v-for="(animal, index) in animals" :key="index">
          <td> {{ animal.sort}}</td>
          <td> {{ animal.name}}</td>
          <td>{{ animal.dateOfBirth..toLocaleString()}}</td>
        </tr>
      </tbody>
    </table>


  </div>
</template>

<script>
export default {
  name: 'AnimalList',
  data() {
    return {
      animals: [
      
          {
            sort: 'pas',
            name: 'panco',
            dateOfBirth: new Date(2020, 7, 15)
          },
          {
            sort: 'macka',
            name: 'mica',
            dateOfBirth: new Date(2019, 8, 19)
          },
          {
            sort: 'krava',
            name: 'kravica',
            dateOfBirth: new Date(2018, 1, 11)
          },
          {
            sort: 'svinja',
            name: 'svinjcek',
            dateOfBirth: new Date(2017, 2, 5)
          },
          {
            sort: 'majmun',
            name: 'majmunko',
            dateOfBirth: new Date(2016, 4, 23)
          }
    
      
      ]
    }
  }
  



}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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

table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width:30%;
  margin-left:35%;
  margin-right:35%; 
}

td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

tr:nth-child(even) {
  background-color: #dddddd;
}
</style>
