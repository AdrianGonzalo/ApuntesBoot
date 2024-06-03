# Introducción a React

## ¿Qué es React?

React es una biblioteca de JavaScript desarrollada por Facebook para construir interfaces de usuario. Es especialmente útil para construir aplicaciones de una sola página (Single Page Applications, SPA) donde se necesita actualizar datos sin recargar toda la página.

## Principales Características

1. **Componentes**:
   - React está basado en componentes. Un componente es una pieza de la interfaz de usuario.
   - Los componentes pueden ser de clase o funcionales.
   - Los componentes pueden ser reutilizables, anidados y administran su propio estado.

2. **JSX (JavaScript XML)**:
   - Es una extensión de la sintaxis de JavaScript que permite escribir HTML directamente en JavaScript.
   - JSX se convierte a JavaScript puro mediante herramientas como Babel.

3. **Estado y Props**:
   - **Estado**: Es un objeto que contiene datos que afectan el renderizado del componente.
   - **Props**: Son argumentos que se pasan a los componentes para configurar su comportamiento y apariencia.

4. **Virtual DOM**:
   - React usa un Virtual DOM para mejorar el rendimiento. Solo las partes de la interfaz que cambian se vuelven a renderizar.

5. **Unidirectional Data Flow (Flujo de Datos Unidireccional)**:
   - Los datos fluyen en una única dirección, de los componentes padres a los hijos, lo que facilita el seguimiento y la gestión del estado.

## Instalación y Configuración

Para comenzar con React, necesitas tener Node.js y npm (Node Package Manager) instalados. Puedes crear una nueva aplicación de React usando Create React App, que es una herramienta oficial para configurar un proyecto React.

```bash
npx create-react-app my-app
cd my-app
npm start