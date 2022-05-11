<template>
  <div>
    <form @submit.prevent="submitData">
      <input v-model="name" />
      <input v-model="age" />
      <button v-on:click="addUser">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      age: "",
    };
  },
  emits: ["add-user-data"],
  method: {
    submitData() {
      console.log(this.name, this.age);
      this.$emit("add-user-data", this.name, this.age);
    },
  },
};
</script>


<style>
</style>