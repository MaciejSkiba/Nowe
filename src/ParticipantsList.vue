<template>
  <div>
    <ol>
        <li :key="person" v-for="person in list">
            {{person}}
        </li>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list']
  };
</script>
