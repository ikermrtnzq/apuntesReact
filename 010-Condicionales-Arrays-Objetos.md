# CONDICIONALES

```js
this.valor == 0 && (<h1>ES 0 </h1>)
```

```js
this.valor == 0 ? (<h1>ES 0 </h1>): (<h1>ES 0 </h1>)
```

```js
this.valor == 0 ? <h1>ES 0 </h1>:
```

```js
this.valor >= 0 ? <h1>ES mayor a 0 </h1>: <h1>ES negativa </h1>
```

# ARRAYS DE OBJETOS

```js
state ={
    comics: [
        {
            titulo: "Spiderman",
            imagen: "https://3. ",
            descripcion: "Hombre araña"
        },
        {
            titulo: "Wolverine",
            imagen: "https://images-na.ssl-imag ",
            descripcion: "Lobezno"
        }
    ],
    favorito: null
}
```

## MAP

```jsx
this.state.comics.map((comic, index) =>{
    return(
        <Comic key={index} comic={comic} seleccionarComic={this.seleccionarComic} deleteComic={this.deleteComic} index={index}></Comic>
    )
})
```

## DELETE

```js
deleteComic = (index) => {
    this.state.comics.splice(index,1)
    this.setState({
        comics: this.state.comics
    })
}
```

```jsx
<button onClick={() => this.props.deleteComic(this.props.index)}>-</button>
```
