<template>
  <form>
    <input type="text" v-model="title" name="title" placeholder="Add a Todo" />
    <input class="btn" type="submit" value="Submit" />
  </form>
</template>

<script>
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
    };
  },
};
</script>

<style scoped>
form {
  display: flex;
}

input[type="text"] {
  flex: 10;
  padding: 5px;
}

input[type="submit"] {
  flex: 2;
}
</style>