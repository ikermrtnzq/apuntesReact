# COMPONENTES, PROPS Y MÉTODOS

## Props

Un prop sirve para podernos comunicarnos de **PADRE a HIJO**.

### Desde el padre

```jsx
<Saludo mensaje="hola hijoo"/>
```

### Lo recibimos desde el hijo

```js
function Saludo(props){
    let mensaje = props.mensaje;
    return()
}

export default Saludo;
```

### Podemos declarar props de seguido

```js
const {nombre, edad} = props;
```

---

## Cómo declarar un MÉTODO en un COMPONENT

```js
const doble = (numero) => {
    console.log(" Resultado = " + numero*2)
}
```

### Llamarlo en un botón

```jsx
<button onClick={() => incrementarContador()}>incrementar</button>
```

### Llamarlo sin necesidad de un botón

```jsx
{incrementarContador()}
```

### Los MÉTODOS pueden recibir parámetros

```js
const metodoPadre = (nombre, id) => {
    console.log("Yo soy tu padre: " + nombre + " con id: " + id)
}
```

```jsx
<button onClick={() => metodoPadre(mensaje, id)}>llamar</button>
```
