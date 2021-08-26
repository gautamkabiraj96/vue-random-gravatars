<template>
  <div>
    <h2>Named Avatars</h2>
    <div v-for="(name, index) in names" :key="index" class="list-style">
      <Avatar v-bind:initials="name.firstName + name.lastName" />
      {{ name.firstName }} {{ name.lastName }}
    </div>
  </div>
</template>
 
<script>
import Avatar from "./Avatar";

export default {
  name: "MainComponent",
  components: {
    Avatar,
  },
  data() {
    return {
      names: [
        {
          id: 1,
          firstName: "Gautam",
          lastName: "Kabiraj",
        },
        {
          id: 2,
          firstName: "Emma",
          lastName: "Parker",
        },
        {
          id: 3,
          firstName: "Jane",
          lastName: "Oliver",
        },
        {
          id: 4,
          firstName: "Kane",
          lastName: "Lee",
        },
        {
          id: 5,
          firstName: "Jim",
          lastName: "Ko",
        },
        {
          id: 6,
          firstName: "Tina",
          lastName: null,
        },
      ],
    };
  },
};
</script>

<style scoped>
.list-style {
  border: 1px solid rgb(201, 235, 255);
  background: rgb(239, 248, 255);
  padding: 10px 8px;
  margin: 10px 0;
  text-align: left;
}
</style>