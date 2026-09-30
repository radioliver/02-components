<script setup>
import { ref } from 'vue';
    defineEmits(['on-input']);

    defineProps({
        modelValue: {
            type: String,
            required: false,
            default: ''
        },
        id: {
            type: String,
            required: true
        },
        type: {
            type: String,
            default: '  text'
        },
        placeholder: {
            type: String,
            default: ''
        },
        label: {
            type: String,
            default: ''
        }

        
        
    });

    const name = ref('');

</script>

<template>
    <label :for="id">{{label}}:</label>
    <input 
    v-model = "name" 
    :value="modelValue"
    :id="id"
    :type="type" 
    :placeholder="placeholder" 
    @input="$emit('on-input', $event.target.value)" />
</template>

<style scoped>
</style>
