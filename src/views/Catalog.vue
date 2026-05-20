<template>
  <div>
    <h2>Catalogo</h2>
    <ul>
      <li v-for="articulo in articulos" :key="articulo.identificador">
        <RouterLink :to="{ name: 'Producto', params: { identificador: articulo.identificador } }">
          {{ articulo.nombre }}
        </RouterLink>
      </li>
    </ul>
  </div>
</template>

<script setup>
const articulos = [
  { identificador: 1, nombre: 'Articulo Uno' },
  { identificador: 2, nombre: 'Articulo Dos' },
  { identificador: 3, nombre: 'Articulo Tres' }
]
</script>
