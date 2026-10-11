<template>
<div class="card">
  <h3>{{ titulo }}</h3>
  <p>{{ descricao }}</p>
</div>
</template>

<script setup>
const props = defineProps({
titulo: String,
descricao: String
})
</script>

<style scoped>
.card {
background-color: #0F2E1D;
color: #D4A94A;
border: 1px solid #D4A94A;
border-radius: 8px;
padding: 1rem;
text-align: center;
}
</style>
