# HTML

HTML (HyperText Markup Language) es el lenguaje estándar para crear y diseñar páginas web. Aquí están algunos de los métodos y elementos más utilizados:

## Estructura básica

```html
<!DOCTYPE html>
<html>
<head>
    <title>Título de la página</title>
</head>
<body>
    Contenido de la página
</body>
</html>
```
## Encabezados

```html
<h1>Título 1</h1>
<h2>Título 2</h2>
<h3>Título 3</h3>
```

## Parrafos

```html
<p>Este es un párrafo.</p>
```

## Enlaces

```html
<a href="https://www.ejemplo.com">Este es un enlace</a>
```

## Imágenes

```html
<img src="ruta/de/la/imagen.jpg" alt="Descripción de la imagen">
```

## Listas

#### · No ordenadas

```html
<ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
</ul>
```

#### · Si ordenadas

```html
<ol>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
</ol>
```

## Tablas

```html
<table>
    <tr>
        <th>Encabezado 1</th>
        <th>Encabezado 2</th>
    </tr>
    <tr>
        <td>Dato 1</td>
        <td>Dato 2</td>
    </tr>
</table>
```

## Formularios

```html
<form action="/ruta/del/servidor" method="post">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">
    <input type="submit" value="Enviar">
</form>
```

## Botones

```html
<button>Botón estándar</button>
<button type="button" onclick="alert('¡Hola!')">Botón con acción</button>
<input type="button" value="Botón input">
```

## Video

```html
<video width="320" height="240" controls>
    <source src="movie.mp4" type="video/mp4">
    Tu navegador no soporta el elemento de video.
</video>
```

## Audio

```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Tu navegador no soporta el elemento de audio.
</audio>
```

[All Documentation](https://developer.mozilla.org/es/docs/Web/HTML)