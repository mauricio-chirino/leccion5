<template>
  <div>
    <h2>Detalle del articulo</h2>
    <p>Identificador recibido: {{ identificador }}</p>
  </div>
</template>

<script setup>
defineProps({
  identificador: String
})
</script>
