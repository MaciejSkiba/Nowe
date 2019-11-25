<template>
  <div>
    <h1>{{ title }}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {title: 'Clicked 0 times'}
    },
    methods: {
      iAmClicked() {
        this.title= 'Clicked';
      }

    }
  };
</script>
