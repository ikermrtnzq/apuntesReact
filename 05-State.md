# STATE

Por cuestiones de recursos, React no dibuja los elementos en el Render al cambiar los valores de la página.

Nuestro component NO sabe que han sido cambiadas y no redibuja nuestro component.

Para eso usamos los **STATE**.

Los estados de un component son varios:

* Cargar un component
* Update del component
* Destruir un component

## Tenemos 2 métodos

* **Get:** Cuando recuperamos el valor de una variable.
* **Set:** Cuando establecemos el valor de una variable.

## Importar STATE

Para poder usar STATE primero tenemos que importarlo:

```js
import {useState} from 'react';
```

## Declarar la variable

El primer valor es el **get** y el segundo el **set**:

```js
const [numero,setNumero] = useState(5);
```

## Usarlo

```js
setNumero(numero+1)
```
