# sol for https://vuejs.org/tutorial/#step-2

<script>
export default {
  data() {
    return {
      message: "Harsh Shukla"
    }
  }
}
</script>

<template>
  <h2>Hello, I am {{ message}}</h2>
  <em>My Name In Reverse!</em>
  <strong><p>{{ message.split(' ').reverse().join(' ') }}</p></strong>
</template>