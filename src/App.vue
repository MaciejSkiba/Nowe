<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ol  v-if="people.length > 0">
        <li :key="person" v-for="person in people">{{person}}</li>
      </ol>
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
  export default {
    data() {
      return {
        people: [
          "Ktoś Tam"
        ],
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
