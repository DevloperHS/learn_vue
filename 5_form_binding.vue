# sol for https://vuejs.org/tutorial/#step-5

<!--

Data Flow: Data -> Methods -> Trigger (v-model) -> Update Data -> Update DOM

In this example, we have a data property called `msg` that is initialized to an empty string. We use the `v-model` directive on the input element to create a two-way binding between the input's value and the `msg` data property.

When the user types into the input field, the `v-model` directive automatically updates the `msg` data property with the current value of the input. This change in data then updates the DOM to display the new value of `msg` in the paragraph element below.


-->

<script>
export default {
  data() {
    return {
      text: '',
      msg:''
    }
  },
  methods: {
    onInput(e) {
      this.text = e.target.value
    },
    
    // onInput2(e) {
    //   this.msg = e.target.value
    // }
  }
}
</script>

<template>
<!--<input :value="text" @input="onInput2" placeholder="Type here">-->
  <input v-model="msg" placeholder="Type here">
  <p>{{ msg }}</p>
</template>