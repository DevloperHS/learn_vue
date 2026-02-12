# sol for https://vuejs.org/tutorial/#step-3

<script>
export default {
    data() {
        return {
            titleClass: 'title' // this is the name of the class we want to apply to the element
        }
    }
}
</script>

<template>
    <h1 v-bind:class="titleClass">Make me red</h1>
    <!-- above binding is on style .title , this is why we are using :class, rather than :id-->
    <!-- the The part after the colon (:class) is the "argument" of the directive.  -->
    <!--titleClass act as a compoenent state variable (stored in data property) that holds the class name to be applied to the element -->
</template>

<style>
.title {
    color: red;
}
</style>