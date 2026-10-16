
# ASYNC / AWAIT EN SERVICIOS

En vez de devolver promesas podemos usar `async` / `await`.

## Función del servicio

```jsx
async obtenerHospitales() {
    let url = Global.urlApiTrabajadores;
    let endpoint = "/"

    try {
        let response = await axios.get(url + endpoint);
        return response.data;
    } catch(error) {
        throw error;
    }
}
```

## Acceder a la función desde el componente

```jsx
cargarHospitales = async() => {
    let datos = await this.service.obtenerHospitales();

    this.setState({
        hospitales: datos
    })
}
```
