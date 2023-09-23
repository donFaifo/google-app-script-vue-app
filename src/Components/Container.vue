<script setup>
import { defineProps, ref } from 'vue';

const props = defineProps({
  title: String
})
</script>

<template>
  <div class="p-3 m-2 border rounded-lg border-gray-700 shadow-md">
    <div>{{ props.title }}</div>
    <slot></slot>
  </div>
</template>