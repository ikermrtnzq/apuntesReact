# FORMULARIOS EN REACT

Los formularios son variables de React.

## Capturar y acceder al valor

```jsx id="wpxv01"
<form onSubmit={this.recibirInfo}>
    <label>Nombre:</label>
    <input type="text" ref={this.cajaNombre}></input>
    <button>Enviar info</button>
</form>
```

```js id="67w1ej"
cajaNombre = React.createRef();

recibirInfo =(event) => {
    event.preventDefault();
    console.log("enviado: " + this.cajaNombre.current.value)
}
```

## Bucle y condicional fuera del render

```js id="knz3wx"
while(numero != 1){
    if(numero%2 == 0){
        numero = numero/2;
    }else{
        numero= (numero*3)+1;
    }
    aux.push(numero);
}
```

## Multi-select

```jsx id="4em3n9"
<h3 style={{color: "red"}}>{this.state.seleccionados}</h3>
<form onSubmit={this.mostrarSeleccionados}>
    <label>Seleccione:</label><br></br>
    <select size="3" multiple ref={this.selectMultiple}>
        <option>elemento 1</option>
        <option>elemento 2</option>
        <option>elemento 3</option>
        <option>elemento 4</option>
        <option>elemento 5</option>
    </select> <br></br>
    <button>Mostrar Elegidos</button>
</form>
```

```js id="2c6gfh"
mostrarSeleccionados = (event) => {
    event.preventDefault();
    let options = this.selectMultiple.current.options;
    let data ="";
    for(var opt of options){
        if (opt.selected){
            data = data + opt.value + ", ";
        }
    }
    this.setState({
        seleccionados: data
    }) 
}
```
