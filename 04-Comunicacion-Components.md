# COMUNICACIÓN ENTRE COMPONENTS

La COMUNICACIÓN ENTRE COMPONENTS es un elemento fundamental dentro de cualquier Framework SPA.

Esta comunicación nos permite realizar components dinámicos y poder modificar cada información que muestra un component.

Por ejemplo, props es la comunicación de un component **PARENT A HIJO**.

La comunicación entre hijo y padre se realiza mediante métodos.

Para lograr la comunicación debemos realizar lo siguiente:

* El component parent tendrá un método (el cual se manda como prop al hijo) y el hijo también tendrá otro método.
* El método del HIJO enviará la información al método del PARENT.

## Método en PARENT y lo pasamos a HIJO como prop

```js id="u1ivna"
const doble = (numero) => {
    console.log(" Resultado = " + numero*2)
}
```

```jsx id="7j2q2k"
<Matematicas metodoPadre1={doble} metodoPadre2={triple}/>
```

## Dentro de HIJO lo recibimos

```js id="gq6w0f"
function Matematicas (props) {

    let numero = "15";
    let doble= props.metodoPadre1;
}
```

## Mandamos la información al padre desde el método

```jsx id="x4v1qo"
<button onClick={() => doble(numero)}>Calcular Doble</button>
```

## Usamos la información que nos ha mandado el HIJO en la función PARENT
