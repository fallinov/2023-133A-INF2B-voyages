<script setup>
defineProps({
  dest: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div>
    {{ dest.nom }} - {{ dest.prix }} CHF
  </div>
</template>

<style scoped>

</style>
