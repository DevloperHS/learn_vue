<!--

Dataflow: Data -> Methods -> Trigger (v-on/ @) -> Update Data -> Update DOM

In this example, we have a data property called `count` that is initialized to 0. We have three methods: `increment`, `decrement`, and `square`, which modify the value of `count`.

In the template, we display the current value of `count` and have three buttons that trigger the respective methods when clicked. When a button is clicked, the corresponding method is called, which updates the `count` data property. This change in data automatically updates the DOM to reflect the new value of `count.

-->

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  
  methods: {
    increment() {
      this.count++;
    },
    
    decrement() {
      this.count--; // no need to assign the result back to count when using increment/decrement operators
    },
    
    square() {
      this.count = this.count ** 2; // need to assign the result back to count to update it
    }
  }
}
</script>

<template>
  <p>Count is: {{ count }}</p>
  <button @click="increment">Add</button><br><br>
  <button @click="decrement">Subract</button><br><br>
  <button @click="square">Square</button>
</template>