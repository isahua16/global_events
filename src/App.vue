<template>
  <div id="app">
    <user-list></user-list>
    <special-user></special-user>
    <all-users></all-users>
  </div>
</template>

<script>
import UserList from '@/components/UserList.vue'
import SpecialUser from '@/components/SpecialUser.vue'
import AllUsers from '@/components/AllUsers.vue'

export default {
  name: 'App',
  components: {
    UserList,
    SpecialUser,
    AllUsers
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
