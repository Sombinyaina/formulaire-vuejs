<template>
  <div id="app">
  <AddForm v-if="!showLoading" v-on:addUser = "addUser"/>
  <UserCard v-if="!showLoading" v-bind:allUsers="users" msg="my message"/>
  <WaitSpinner v-if="showLoading"/>
  <ModalForm />
  <button v-if="!showLoading" v-on:click="handleToogle">Toggle</button>
  <button >Click</button>
  </div>
</template>

<script>

import WaitSpinner from './components/WaitSpinner.vue';
import UserCard from './components/UserCard.vue';
import AddForm from './components/AddForm.vue';
import ModalForm from './components/ModalForm.vue';
export default {
  name: 'App',
  components: {
   AddForm,UserCard,WaitSpinner,ModalForm
  },
  methods: {
    addUser (newUser) {
      console.log(newUser);
      this.users.push(newUser);
    },
    handleToogle (){
      // console.log("clicked");
      this.showLoading = !this.showLoading
    },
    modalCard () {
    }
  },
  data() {
    return {
      users : [],
    showLoading : true,
    }
  },
  mounted() {
    console.log("app mounted");
    this.showLoading = true;
    setTimeout(() => {
      console.log("after 2 secound");
      this.showLoading = false;
    }, 2000);
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
