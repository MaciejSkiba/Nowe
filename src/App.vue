<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <Participants-list :list="people"></Participants-list>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text" v-model="Firstname">
      <label>Lastname</label>
      <input type="text" v-model="Lastname">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
import ParticipantsList from "./ParticipantsList.vue";
  export default {
    components: {ParticipantsList},
    data() {
      return {
        people: [],
        Firstname:"",
        Lastname:""
      };
    },
    methods: {
      addNewParticipant() {
        if(this.Firstname.length >0 && this.Lastname.length >0)
        {
        this.people.push(this.Firstname + " " + this.Lastname);
      };
      this.Firstname="",
      this.Lastname=""
      }
    }
  };
</script>
