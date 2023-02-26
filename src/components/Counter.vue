<template>
  <div>
    <h2>{{ count }}</h2>
    <button @click="changebuttonvalue">Change</button>
    <button @click="toggleCount">{{ buttonlabel }}</button>

  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      buttonlabel: "Increment"
    };
  },
  methods: {
    toggleCount() {
    if (this.buttonlabel === "Increment") {
      this.increment();
    } else if (this.buttonlabel === "Decrement") {
      this.decrement();
    }
  },
    increment() {
      this.count++;
    },

    decrement(){
      this.count--;
    },

    changebuttonvalue() {
     this.buttonlabel = this.buttonlabel === "Increment" ? "Decrement" : "Increment";
    }

  }
};
</script>

<style scoped>
h2 {
  font-size: 3rem;
  margin: 0;
  text-align: center;
}

button {
  font-size: 1.5rem;
  padding: 1rem;
  margin: 1rem;
  border: none;
  border-radius: 0.25rem;
  background-color: #4caf50;
  color: #fff;
}
</style>
