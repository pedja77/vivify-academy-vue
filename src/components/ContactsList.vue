<template>
  <div>
   <ul>
     <table>
       <thead>
         <th>First Name</th>
         <th>Last Name</th>
         <th>Email</th>
       </thead>
       <tbody>
         <tr v-for="(user, key) in users" :key="key">
          <td>{{user.firstName}}</td>
           <td>{{user.lastName}}</td>
           <td>{{user.email}}</td>
         </tr>
       </tbody>
     </table>
   </ul>
  </div>
</template>

<script>
export default {
  name: 'ContactsList',
  data() {
    return {
      users: [
        {firstName: 'Pedja', lastName: 'Smigeljski', email: 'p@p.p'},
        {firstName: 'Viki', lastName: 'Rakic', email: 'v@v.v'}, 
        {firstName: 'Sofronije', lastName: 'Leghorn', email: 's@s.s'}
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
</style>
