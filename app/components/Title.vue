<template>
  <component :is="level" :class="customClass">
    {{ text }}
  </component>
</template>

<script setup>
defineProps({
  text: {
    type: String,
    required: true,
  },
  level: {
    type: String,
    default: 'h2', // h1, h2, h3, ...
    validator: (value) => ['h1', 'h2', 'h3', 'h4', 'h5', 'h6'].includes(value),
  },
  customClass: {
    type: String,
    default: 'title-1',
    validator: (value) => ['title-1','title-2'].includes(value),
  },
})

</script>
