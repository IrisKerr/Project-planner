<template>
  <form>
    <label for="title">Title:</label>
    <input type="text" v-model="title" id="title" required />
    <label for="details">Details:</label>
    <textarea v-model="details" id="details" required></textarea>
    <button>Update Project</button>
  </form>
</template>

<script>
export default {
  props: ["id"],
  data() {
    return {
      title: "",
      details: "",
      uri: "http://localhost:3000/projects/" + this.id,
    };
  },
  // when component mounts, we can fetch the data of the project within it's id to pre-populate the edit form
  mounted() {
    fetch(this.uri)
      .then((res) => res.json())
      .then((data) => {
        this.title = data.title;
        this.details = data.details;
      });
  },
};
</script>

<style></style>
