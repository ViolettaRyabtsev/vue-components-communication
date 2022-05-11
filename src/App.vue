
<template>
  <div>
    <user-data @add-user-data="addUser"></user-data>
    <ul>
      <active-user
        v-for="user in usersData"
        :key="user.id"
        :name="user.name"
        :age="user.age"
      ></active-user>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      usersData: [
        {
          name: "violet",
          age: "32",
        },
      ],
    };
  },
  methods: {
    addUser(name, age) {
      let objectUser = {
        name: name,
        age: age,
      };

      console.log(objectUser, "where");

      this.usersData.push(objectUser);
    },
  },
};
</script>

<style >
</style>
