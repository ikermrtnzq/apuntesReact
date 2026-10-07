# OBJETOS

Un objeto es una variable compuesta por múltiples propiedades, por ejemplo, una persona.

```js id="mjd2b4"
let coche ={
    marca : props.marca,
    modelo: props.modelo,
    velocidadmaxima: parseInt(props.velocidadMaxima),
    aceleracion: parseInt(props.aceleracion)
}
```

## Podemos almacenar objetos en STATE

```js id="d6m9xz"
const [coche,setCoche] = useState({});
```

## Utilizar sus propiedades

```js id="v8q2na"
if(velocidad < coche.velocidadmaxima)
```

## Pintarlas en el HTML

```jsx id="w4j1kp"
<h1>{coche.marca} {coche.modelo}</h1>
```
