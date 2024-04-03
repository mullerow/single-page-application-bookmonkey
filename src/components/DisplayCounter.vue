<template>
  <h2>counter: [{{ counter }}]</h2>
  <button @click="increaseCount">Click ME!</button>
</template>

<script>
export default {
  name: "DisplayCounter",
  props: {
    counter: Number,
  },
  methods: {
    increaseCount() {
      this.$emit("increase", this.counter);
      // this.count++;
    },
  },
};
</script>

<style scoped>
button {
  width: 200px;
  height: 30px;
  background-color: lightcoral;
  border-radius: 10px;
}
</style>
