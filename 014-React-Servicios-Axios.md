# REACT SERVICIOS

Los formatos estándar son:

* JSON
* XML

## Métodos de API

* **GET:** Recuperar datos.
* **POST:** Crear elementos en la API o enviar información. Por ejemplo, login con información encriptada y recuperar.
* **PUT:** Modificar.
* **DELETE:** Eliminar datos.

## Fetch y Axios

Fetch es nativo de JS.

Axios es una librería.

Para instalar Axios:

```bash id="3zqv6f"
npm install --save axios
```

Funciona para múltiples Fronts, pero hay que instalarlo.

Las peticiones a las API son asíncronas.

Utilizamos promesas porque no sabemos cuánto va a tardar en llegar la respuesta.

## Importar Axios

```js id="e8p5rs"
import axios from 'axios';
```

## STATE

```js id="5z8j1v"
state = {
    customers: []
}
```

## URL

```js id="f3r6by"
url="https://services.odata.org/V4/Northwind/Northwind.svc/Customers"
```

## GET

```js id="2tbi56"
loadCustomer = () => {
    axios.get(this.url).then((response) => {
        console.log("leyendo")
        //LOS DATOS VIENEN DENTRO  de data.
        this.setState({
            customers: response.data.value
        })
    })
}
```

## MAP de customers

```jsx id="rlgn2g"
{
    this.state.customers.map((customer, index) => {
        return(
            <h4 key={index}>contacto: {customer.ContactName} </h4>
        )
    })
}
```

## React.StrictMode

Quitar `<React.StrictMode>` de `index.js` para evitar que la petición a la API se haga dos veces.

## Global.js

```js id="4enwh3"
var Global ={
    url : "https://services.odata.org/V4/Northwind/Northwind.svc/ "
}
export default Global
```

Cambiar una variable en un único archivo evita tener que cambiarla archivo por archivo.

## Utilizar Global

```js id="vf0oi2"
import Global from '../Global'
let request="suppliers"
axios.get(Global.url + request).then((response) => {}
```

## Set

```js id="159u1z"
let lista = new Set([])
for(var emp of response.data){
    lista.add(emp.oficio)
}
this.setState({
    oficios: Array.from(lista)
})
```

También se puede hacer:

```js id="e4xi37"
let lista = [...new Set(response.data.map(elem => elem.oficio))];
```
