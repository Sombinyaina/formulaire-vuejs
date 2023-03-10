<template>
  <div>
    <form action="" v-on:submit.prevent="handleAddUser" class="formulaire">
      <div class="form-example">
        <label for="name">Name </label>
        <input type="text" name="name" id="name" v-model="name" />
      </div>
      <div class="form-example">
        <label for="email">Age </label>
        <input type="text" name="email" id="email" v-model="age" />
      </div>
      <div class="form-example">
        <label for="role">Role </label>
        <input type="text" name="role" id="role" v-model="role" />
      </div>
      <div class="form-example">
        <button type="submit">ADD</button>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  name: "AddForm",
  data: function () {
    return {
      name: "",
      age: "",
      role: "",
    };
  },
  methods: {
    handleAddUser() {
      console.log(this.name);
      console.log(this.age);
      console.log(this.role);
      this.$emit("addUser", {
        name: this.name,
        age: this.age,
        role: this.role,
      });
    },
  },
};
</script>
<style></style>
