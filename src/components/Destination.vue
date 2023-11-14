<script setup>
defineProps({
  pDest: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div>
    {{ pDest.nom }} - {{ pDest.prix }} CHF
  </div>
</template>

<style scoped>

</style>
