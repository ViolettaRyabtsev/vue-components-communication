<template>
  <li>
    <h3>user active</h3>
    <h3>{{ name }}</h3>
    <h3>{{ age }}</h3>
  </li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    age: {
      type: String,
      required: true,
    },
  },
};
</script>


<style>
</style>