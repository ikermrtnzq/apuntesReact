# ARRAYS

Podemos declarar ARRAYS y añadimos valores por medio de BUCLES:

```js id="a20n3y"
dibujarNumeros = () => {
    let lista =[];
    for(let i = 1; i<= 7; i++){
        var num= parseInt(Math.random()*120)+1
        lista.push(<li>key {i}, {num}</li>)
    }
    return lista;
}
```

```jsx id="kwf899"
<ul>{this.dibujarNumeros()}</ul>
```

## Array en STATE

```js id="04be74"
state = {
    nombres: ["Mara", "Sofia", "Juan"]
}
```

## Añadir elementos

```js id="04be74"
generarNombres = () => {
    //AÑADIMOS
    this.state.nombres.push("Marcos")
    //Es ncesario hacer setState para ACTUALIZAR 
    this.setState({
        'nombres' : this.state.nombres
    })
}
```

## MAP

```js id="vukhf0"
render(){
    return(<div>
        <h1>Dibujo con render</h1>
        <button onClick = {this.generarNombres}>generar</button>
        {
            this.state.nombres.map((nombre, index) => {
                return(<h3 key={index}> {nombre}</h3>)
            })   
        }
    </div>)
}
```

Se puede añadir código directamente en el render, lo que está entre llaves `{}`, puede ir en una función arriba(el MAP sería sustituido por un FOR).
