<template>
  <div>
    <div class="card" v-for="(user, index) in allUsers" :key="index">
      <div>{{ msg }}</div>
      <p>{{ user.name }}</p>
      <p>{{ user.age }}</p>
      <p>{{ user.role }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "UserCard",
  props: ["allUsers", "msg"],
};
</script>
<style>
.card{
    border-bottom: 1px black solid;
}
</style>
