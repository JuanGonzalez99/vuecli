<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <Persona nombre="Jorge" edad="25"></Persona>
  <hr>
  <Persona nombre="Linda" edad="32"></Persona> -->
  <Usuarios 
    v-for="user in users"
    v-bind:key="user.id"
    :id="user.id"
    :name="user.name"
    :email="user.email"
    :phone="user.phone">

  </Usuarios>
</template>

<script>
import axios from 'axios'
// import Persona from './components/Persona'
import Usuarios from "./components/Usuarios";

export default {
  name: 'App',
  components: {
    // Persona,
    Usuarios
  },
  data(){
    return {
      users: []
    }
  },
  methods:{
    getUsers(){
      axios.get('https://jsonplaceholder.typicode.com/users')
        .then((response) => {
          this.users = response.data;
        });
    }
  },
  mounted(){
    this.getUsers();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
