<template>
  <button @click="e => $emit('click', e)"><slot /></button>
</template>

<script>
export default {
}
</script>

<style scoped>
button {
  padding: 10px 20px;
  background: greenyellow;
  border-radius: 20px 5px;
  border: none;
  outline: none;
  color: #181818;
  font-weight: bold;
  text-transform: uppercase;
  font-family: "Quicksand", sans-serif;
  font-size: 0.7rem;
}
</style>


