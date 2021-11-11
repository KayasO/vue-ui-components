<template>
  <div id="counter">
    <h1>Counter</h1>
    <p>Counter: {{ counter }}</p>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  data() {
    return {
      counter: 0,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
