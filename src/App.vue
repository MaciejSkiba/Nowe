<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <h3>New participant</h3>
      <form @submit.prevent="addNewParticipant()">
        <label>Firstname </label>
        <input type="text">
        <label>Lastname </label>
        <input type="text">
        <button>Add new participant</button>
      </form>
      <ol v-if="numbers.length > 0">
        <li: key="number" v-for="number in numbers">{{Firstname}{Lastname}}
      </ol>
    </div>
  </div>

</template>

<script>
  export default {
    data() {
      return {numbers:[]};
    },
    methods: {
      addNewParticipant() {

      }
    }
  };
</script>
