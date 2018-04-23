<template>
  <div>
    <form @submit.prevent="addUser">
      <label for="first-name">First name</label>
      <input type="text" id="first-name" v-model="newUser.firstName">
      <label for="last-name">Last name</label>
      <input type="text" id="last-name" v-model="newUser.lastName">
      <label for="email">Email</label>
      <input type="text" id="email" v-model="newUser.email">
      <button type="submit">Submit</button>
    </form>
     <table>
       <thead>
         <th>First Name</th>
         <th>Last Name</th>
         <th>Email</th>
         <th>&nbsp;</th>
       </thead>
       <tbody>
         <tr v-for="(user, key) in users" :key="key">
           <td>{{user.firstName}}</td>
           <td>{{user.lastName}}</td>
           <td>{{user.email}}</td>
           <td><button @click="deleteUser(key)">x</button></td>
         </tr>
       </tbody>
    </table>
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
        ],
      newUser: {
        firstName: '',
        lastName: '',
        email: ''
      }
    }
  },
  methods: {
    addUser() {
      //console.log(event);
      this.users.push(this.newUser);
      this.newUser = {} // nova referenca na objekat newUser, ispraznimo inpute
    },
    deleteUser(index) {
      this.users.splice(index, 1);
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
