# ESTILOS

Podemos declarar estilos de 3 maneras.

## EXTERNOS

```js
import './SumarNumeros.css';
```

```jsx
<button className="boton">pulsa</button>
```

## EN VARIABLES

```js
var estilo = {
    color: "red",
    backgroundColor: "yellow"
}
```

```jsx
return (
    <div>
        <h1 style={estilo}>Métodos doble número</h1>
    </div>
)
```

## INLINE

```jsx
<h2 style={{color: "blue"}}>{mensaje}</h2>
```
