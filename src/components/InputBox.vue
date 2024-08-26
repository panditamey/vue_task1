<script setup>
    import { ref } from 'vue';
    let name = ref('');
</script>
<template>
    <div>
        <label for="name">Name</label>
        <!-- v-bind : Binds the value to the name variable -->
        <input type="text" id="name" v-model="name">
        <br>
        <label>{{ name }}</label>
    </div>
</template>