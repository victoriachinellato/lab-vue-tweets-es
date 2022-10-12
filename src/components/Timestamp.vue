<template>
    <span class="timestamp">{{props.timestampPrueba}}</span>
</template>
<script setup>

import { defineProps } from 'vue'; 

const props = defineProps (['timestampPrueba'])

</script>
<style scoped>
</style>