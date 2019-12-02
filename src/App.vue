<template>
  <div>
    <h1>Clicked {{ count }} times.</h1>
    <button @click="increase()">More</button>
    <button @click="resetcounter()">Reset</button>
  </div>
</template>

<script>
    export default {
        data() {
            return {
            title: 'Not clicked yet',
            count:0
            }

        },
        methods: {
            increase() {
                this.count = this.count+1;

            },
            resetcounter(){
            this.count=0;
            }
        }
    };
</script>
