# 🎸 GuitarLA

Tienda de guitarras con carrito de compras interactivo construida con React y Vite. Permite explorar un catálogo de 12 guitarras, agregar productos al carrito, ajustar cantidades y ver el total en tiempo real. El carrito persiste entre sesiones gracias a `localStorage`.

## 🌐 Demo

🔗 [https://guitarla-andremdevco.netlify.app/](https://guitarla-andremdevco.netlify.app/)

## 📁 Archivos principales

| Archivo | Descripción |
|---|---|
| `App.jsx` | Componente raíz. Consume el hook `useCart` y distribuye el estado a los componentes hijos |
| `Header.jsx` | Header con carrito desplegable, tabla de productos y total calculado |
| `Guitar.jsx` | Tarjeta de producto con imagen, nombre, precio y botón para agregar al carrito |
| `useCart.js` | Custom hook que encapsula toda la lógica y el estado del carrito |
| `db.js` | Base de datos local con el catálogo de 12 guitarras |

## 🛠️ Tecnologías utilizadas

![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=white)

## ✨ Características

- **Catálogo de guitarras** — 12 productos con imagen, nombre, descripción y precio
- **Carrito desplegable** — Accesible desde el header, muestra los productos seleccionados con imagen y precio
- **Control de cantidad** — Botones para aumentar o disminuir unidades por ítem (mín. 1 — máx. 5)
- **Eliminación de productos** — Botón para remover un ítem individual del carrito
- **Vaciado del carrito** — Botón para limpiar todos los productos de una sola vez
- **Total en tiempo real** — Calculado con `useMemo` a partir de la cantidad y precio de cada ítem
- **Persistencia con localStorage** — El carrito se mantiene al recargar la página
- **Lazy initializer en `useState`** — El carrito lee `localStorage` solo en el primer renderizado
- **Extracción de lógica de estado a un custom hook (`useCart`) para separar lógica de presentación

## 📚 Conceptos practicados

- Gestión de estado con `useState` y lazy initializer
- Estado derivado con `useMemo` para evitar recálculos innecesarios
- Persistencia del carrito con `useEffect` — guarda el estado en `localStorage` ante cada cambio
- Comunicación entre componentes mediante props y funciones callback
- Manipulación de arreglos con métodos funcionales (`map`, `filter`, `findIndex`, `reduce`)
- Arquitectura de componentes en React con separación de responsabilidades

## 🚀 Cómo ejecutar el proyecto

```bash
git clone https://github.com/andresmdevco/react-guitar-shopping-cart.git
cd react-guitar-shopping-cart
npm install
npm run dev
```
