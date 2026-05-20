# leccion5
estructra de directorios
```src/
├─ main.js
├─ App.vue
├─ router/
│   └─ index.js
└─ views/
├─ Home.vue
├─ Catalog.vue
├─ Product.vue
└─ About.vue   (opcional)
---

## ⚙️ Configuración del router (`src/router/index.js`)
```javascript
import { createRouter, createWebHistory } from 'vue-router'
import Home from '../views/Home.vue'
import Catalog from '../views/Catalog.vue'
import Product from '../views/Product.vue'
import About from '../views/About.vue'

const rutas = [
  { path: '/', name: 'Inicio', component: Home },
  { path: '/catalogo', name: 'Catalogo', component: Catalog },
  { path: '/producto/:identificador', name: 'Producto', component: Product, props: true },
  { path: '/inicio', redirect: '/' },
  { path: '/about', name: 'Acerca', component: About, alias: '/acerca' } // opcional
]

const enrutador = createRouter({
  history: createWebHistory(),
  routes: rutas
})

export default enrutador




     
