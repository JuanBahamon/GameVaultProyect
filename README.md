# GameVaultProyect
Proyecto Estructuras de Datos y Algoritmos 2 Gabriela Chavez Aguilera - Sebastián Bustamante López - Juan José Bahamon Lozano
Link de la propuesta gráfica en Figma: 

Plataforma de gaming donde los usuarios pueden comprar juegos digitales, calificarlos, explorar un catálogo completo y encontrar tiendas y cyber cafés cercanos a través de un mapa interactivo.

## 👥 Integrantes

## 🔗 Enlaces

- **Propuesta gráfica (Figma):** https://www.figma.com/design/UP1sXFrNyJf62cQAjJLfv6/Untitled?node-id=0-1&p=f
- **Deploy (Netlify):** 
- **Repositorio:** 

## Tecnologías utilizadas

- React + Vite
- Firebase (Auth, Firestore, Realtime Database)
- React Router DOM
- Leaflet.js
- SASS (CSS Modules)
- Netlify

## Estructuras de datos implementadas

| Estructura | Uso en el proyecto |
| Lista Enlazada | Historial de juegos visitados recientemente |
| Pila | Navegación entre páginas |
| Árbol BST | Filtrado de juegos por rango de precio |
| Montículo Máximo | Ranking de juegos más vendidos |
| Grafo | Sistema de recomendaciones entre juegos |

## Cómo correr el proyecto

```bash
npm install
npm run dev
npm install leaflet react-leaflet
```

## Estructura del proyecto

```
src/
├── helpers/        # Funciones generales y estructuras de datos
├── context/        # Contextos globales (Auth y Carrito)
├── hooks/          # Custom hooks
├── routes/         # Rutas públicas, privadas y de admin
├── pages/          # Páginas de la aplicación
├── components/     # Componentes reutilizables
└── firebase/       # Configuración de Firebase
```
