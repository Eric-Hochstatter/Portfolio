// components/ProjectSection.vue
<template>
  <section class="mb-12">
    <h2 class="text-2xl font-bold mb-4 text-green-700">{{ title }}</h2>
    <div class="text-gray-800 leading-relaxed">
      <slot></slot>
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  }
});
</script>