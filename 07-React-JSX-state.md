# REACT CON JSX ES6

En vez de utilizar Javascript con function, React utiliza una sintaxis denominada JSX/ES6, un código más parecido a Clases, como lenguajes C# o Java.

Al tener sintaxis de clase, existen elementos conocidos en otros lenguajes, tenemos un constructor.

props sigue siendo exactamente igual, con la diferencia que es una variable interna de la clase Component, ya no necesito declarar props en ningún sitio.

Para acceder a los elementos de mi clase se utilizará la palabra clave `this`.

## Component

```js
const {Component} = require("react");

//Extiende de una clase superior
class Contador extends Component {

    //Ya no necesitams poner ni let ni var
    numero = 1;

    //Ya no es necesario poner function
    incremento = () => {

        //Para acceder a cualquier elemento de la clase usamos this
        this.numero += 1;
        console.log(this.numero)
    }

    //La sintaxix para llamar a los metodos cambia
    render(){
        return(
            <div>
                <h1>CONTADOR JSX</h1>
                <p>{this.numero}</p>
                <button onClick={this.incremento}
                >Incrementar</button>
            </div>
        )
    }
}

export default Contador;
```

## STATE

El funcionamiento de STATE es distinto.

No se utiliza useState.

En su lugar, se declara un objeto de tipo `state = {}` con todas las variables que quiero que sean utilizadas en el render:

```js
state = { 
    velocidad: 0,  
    estado: false,  
    coche: { 
        marca: "Audi", 
        modelo: "Q8" 
    } 
}
```

Posteriormente, dentro de mi clase, puedo acceder a cualquier objeto de state simplemente utilizando:

```jsx
{this.state.velocidad}
{this.state.coche.marca}
```

STATE es de solo lectura, no podemos modificar sus datos directamente, solamente acceder a ellos.

Si queremos cambiar el valor:

```js
this.setState( {velocidad: 200} )
```

## Incrementar valor

```js
incrementarValor = () => {
    this.setState({
        valor: this.state.valor + 1
    })
}
```

## STATE con props

```js
state = { 
    valor : parseInt(this.props.inicio)
}
```
