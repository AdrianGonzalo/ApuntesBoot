# Usos CSS

# Display

*La propiedad display en CSS se usa para controlar cómo se muestra un elemento en la página web.*

**Inline**: Se coloca en horizontal. Se adapta añ ancho del contenido ignora *width* o *heigth*

**Block**: Se apila en vertical, ocupa todo el ancho disponible de su etiqueta contenedora

**Inline-block**: Combinacion de los dos anteriores, se comporta como *inline* pero no ignora *width* o *heigth*
```
Ejemplo de los 3 anteriormente mencionados

div {
  width: 350px;
  height: 50px;
  color: white;
}

.block {
  display: block;
  background: darkblue;
}

.inline {
  display: inline;
  background: darkred;
}

.inline-block {
  display: inline-block;
  background: indigo;
}

<div class="inline">Elemento inline</div>
<div class="block">Elemento block</div>
<div class="inline-block">Elemento inline-block</div>
```

**Flex**: Modelo de cajas flexibles de CSS, estructuras de 1 dimension

**Inline-flex**: Versión en linea de flex, ocupa solo su contenido

**Grid**: Utiliza cuadriculas o rejillas
```
<div class="grid">
  <div class="item item-1"></div>
  <div class="item item-2"></div>
  <div class="item item-3"></div>
  <div class="item item-4"></div>
  <div class="item item-5"></div>
  <div class="item item-6"></div>
</div>

.grid {
  display: grid;
  grid-template-columns: repeat(3, 200px);
  grid-template-rows: repeat(2, 100px);
  gap: 10px;
}

.item {
  background: deeppink;
}
```

**Inline-grid**: Version en linea de grid, ocupa solo su contenido

**None**: Oculta el elemento visualmente

# Position

*La propiedad position en CSS se utiliza para controlar la ubicación de un elemento en relación con su contenedor o con otros elementos en la página web.*

**Static**: el elemento respeta el flujo de la pagina, no tiene en cuenta top, left, right y bottom
```
.rojo{
  height: 100px;
  width: 100px;
  background-color: red;
  border: 2px green solid;
}

#movido{
  left: 100px;
}
<div class="rojo"></div>
<div id="movido" class="rojo"></div>
<div class="rojo"></div>
```

**Relative**:posicionar un elemento respecto al flujo normal de la página, podemos usar top, left, right y bottom
```
.rojo{
  height: 100px;
  width: 100px;
  background-color: red;
  border: 2px green solid;
}

#movido{
  position: relative;
  left: 100px;
}
<div class="rojo"></div>
<div id="movido" class="rojo"></div>
<div class="rojo"></div>
```
**Absolute**: estan fuera flujo normal de la pagina y tiene como referencia la ventana del navegador, podemos usar top, left, rigth y bottom
```
.rojo{
  height: 100px;
  width: 100px;
  background-color: red;
  border: 2px green solid;
}

#movido{
  position: absolute;
  top: 40px;
  left: 50px;
}
<div class="rojo"></div>
<div id="movido" class="rojo"></div>
<div class="rojo"></div>
```
**Fixed**: estan fuera del flujo normal, toman como referencia la ventana del navegador y no respetan tener contenedor padre
```
.rojo{
  height: 100px;
  width: 100px;
  background-color: red;
  border: 2px green solid;
}

#primerDiv{
  height: 2000px
}

#relativo{
  position: relative;
}

#movido{
  position: fixed;
  top: 40px;
  left: 50px;
}
<div id="primerDiv" class="rojo"></div>
<div id="relativo" class="rojo">
  <div id="movido" class="rojo"></div>
</div>
```
**Inherit**: hereda el valor para esta propiedad del elemento padre.

**Initial**: hace que la propiedad *position* tome su valor por defecto  initial === static

**Sticky**: el elemento actúa como si estuviera posicionado con el valor relative hasta que se alcanza un umbral de desplazamiento,con el cual el elemento pasa a posicionarse como si estuviera posicionado con el valor fixed
```
#marca{
  height: 50px;
  width: 100%;
  background-color: green;
  text-align: center;
}

#marca img{
  height: 100%;
}

#menu{
   position: sticky;
   top: 0; 
   height: 100px;
   width: 100%;
   background-color: red;
}

#contenido{
   height: 1200px;
   width: 100%;
   background-color: yellow;
}
<div id="marca">
  <img src="https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAARpAAAAJDMzZGRhNGMwLTU4YmMtNDdmZi1hMjU5LWIwYTViMjdlNWJmOQ.png">
</div>

<div id="menu"></div>
<div id="contenido">CONTENIDO</div>
```

Sacado de [StackOverflow](https://es.stackoverflow.com/questions/37930/cual-es-la-diferencia-entre-position-relative-position-absolute-y-position)

# Flex Flow Junta las 2 separado por espacio

## Flex-direction

Define la direccion de los elementos en el contenedor
```
Row

Los elementos son colocados en la misma direccion del texto
```
```
Row-reverse

Los elementos son colocados en la direccion opuesta del texto
```
```
Column

Los elementos se colocan de arriba hacia abajo
```
```
Column-reverse

Los elementos se colocan de abajo hacia arriba
```
## Flex-wrap

Distribuye correctamente los elementos
```
Nowrap

Cada elemento se ajusta en una sola linea
```
```
Wrap

Los elementos se envuelven alrededor de lineas adicionales
```
```
Wrap-reverse

Los elementos se envuelven alrededor de lineas adicionales en reversa
```
# Align-  alinea en el eje horizontal/vertical columna
```
Align-items

La propiedad de CSS *align-items* establece el valor align-self sobre todos los descendientes directos de un grupo.

-flex-start:  Alinea elementos a la parte superior del contenedor

-flex-end: Alinea elementos a la parte inferior del contenedor

-center: Alinea elementos en el centro (verticalmente hablando) del contenedor

-baseline: Muestra elementos en la línea base del contenedor

-stretch: Elementos se estiran para ajustarse al contenedor
```
### *align-content* determina el espacio entre las líneas, mientras que *align-items* determina como los elementos en su conjunto están alineados dentro del contenedor. Cuando hay solo una línea, align-content no tiene efecto.
```
Align-content

Controla la alineacion de las lineas flexibles dentro de su contenedor cuando hay espacio adicional en el eje transversal en un diseño de flexbox.

-flex-start:  Las lineas se posicionan en la parte superior del contenedor

-flex-end: Las lineas se posicionan en la parte inferior del contenedor

-center: Las líneas se posicionan en el centro (verticalmente hablando) del contenedor.

-space-between: Las lineas se muestran con la misma distancia entre ellas

-space-around: Las lineas se muestran con la misma separecion alrededor de ellas

-stretch: Las lineas se estiran para ajustarse al contenedor
```
```
Align-self

Alinea los elementos flexibles de la línea flexible actual, reemplazando el valor de *align-items*
```
```
Text-align

Alinea el texto dentro de un elemento en el eje horizontal
```
```
Vertical-align

Controla la alineacion vertical de un elemento en relacion con su linea base
```
# Justify-  alinea en el eje vertical/horizontal columna
```
Justify-content

Controla la alineación de los elementos flexibles dentro de su contenedor flex en el eje principal.

  -flex-start: Alinea los elementos hacia el principio del contenedor

  -flex-end: Alinea los elementos hacia el final del contenedor

  -center: Alinea los elementos en el centro del contenedor

  -space-between: Distribuye equitativamente los elementos en el eje principal, el primer elemento se coloca al principio y el ultimo al final, esto significa que habrá un espacio adicional antes del primer elemento y después del último elemento.

  -space-around: Distribuye equitativamente los elementos en el eje principal, colocando un espacio igual alrededor de cada elemento

  -space-evenly: Distribuye equitativamente los elementos en el eje principal, incluido un espacio igual antes del primer elemento y después del último elemento
```
```
Text-align

Alinea el texto dentro de un elemento en el eje horizontal (izquierda, derecha, centro, justificado).
```
```
Justify-items

Alinea los elementos dentro de un contenedor de cuadrícula en el eje principal.
```
```
Justify-self

Permite anular la alineación predeterminada definida por justify-items para un elemento individual dentro de su contenedor de cuadrícula.
```
## Gap Espacio entre filas y columnas
## Order Reordenar por valor
## Em 
La unidad em hace referencia al tamaño en puntos de la letra que se está utilizando. Si se utiliza una tipografía de 12 puntos, 1em equivale a 12 puntos . El valor de 1ex se puede aproximar por 0.5 em .
# Grid

Se destaca por permitir dividir una página en áreas o regiones principales, por definir la relación en términos de tamaño, posición y capas entre partes de un control construido a partir de primitivas HTML.
```
Span

Define la posicion inicial y final basado en la longitud de columnas deseada
```
## grid-template
```
grid-template-columns

Comenzara por la linea horizontal asignada
```
```
grid-template-rows

Terminara por la linea horizontal asignada
```
___
```
repeat 

Atajo para crear copias   repeat(8, 12.5%);
```
```
fr

unidad de medida para especificar el tamaño de columna y filas en relacion con el espacio disponible en el contenedor principal
```
## grid-area: / / / ;
Engloba grid-colum + grid-row
```
  grid-area: 

    1. grid-row-start

    2. grid-column-start

    3. grid-row-end

    4. grid-column-end
```
### grid-column: / ;
```
grid-column-start

Comenzara por la linea horizontal asignada
```
```
grid-column-end

Terminara por la linea horizontal asignada
```

### grid-row
```
grid-row-start

Comenzara por la linea vertical asignada
```
```
grid-row-end

Terminara por la linea vertical asignada
```



