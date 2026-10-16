
# POST CON AXIOS Y NAVEGACIÓN

## POST con Axios

Sirve para validar/insertar en el servidor:

```jsx
guardarDatos = (event) => {
    event.preventDefault();
    let endpoint = "api/hospitales"
    let url = Global.urlApiHospitales;
    let hospital = {
        idHospital: this.inputID.current.value,
        nombre: this.inputNombre.current.value,
        direccion: this.inputDireccion.current.value,
        telefono: this.inputTlfno.current.value,
        camas: this.inputCamas.current.value
    }
    axios.post(this.url+requestAnimationFrame, hospital).then((response)=>{
        this.setState({
            mesaje: "Creado"
        })
    })
}
```

## Navegar de una página a otra

Podemos navegar de una página a otra una vez hemos terminado la funcionalidad. Para ello usamos una variable `status`:

```jsx
state = {
    status: false
}
```

Cuando hayamos terminado la funcionalidad lo pasamos a `true` y comprobamos en código:

```jsx
{
    this.state.status == true && (<Navigate to="/hospitales"/>)
}
```
