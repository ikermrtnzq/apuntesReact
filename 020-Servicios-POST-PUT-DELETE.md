
# SERVICIOS: POST, PUT Y DELETE

## POST

```jsx
crearHospital(hospital) {
    return new Promise(function(resolve) {
        let url = Global.urlApiHospitales
        let endpoint = "api/hospitales"

        axios.post(url + endpoint, hospital).then((response) => {
            console.log("insertado")
            resolve(response)
        })
    })
}
```

### Llamada desde el componente

```jsx
guardarDatos = (event) => {
    event.preventDefault();

    let hospital = {
        idHospital: parseInt(this.inputID.current.value),
        nombre: this.inputNombre.current.value,
        direccion: this.inputDireccion.current.value,
        telefono: this.inputTlfno.current.value,
        camas: parseInt(this.inputCamas.current.value)
    }

    this.service.crearHospital(hospital).then(result => {
        this.setState({
            status: true
        })
    })
}
```

## Mandar datos por URL y recibirlos por props

```jsx
<td style={{padding: "10px",border : "1px solid #D3D3D3"}}>
    <NavLink to={"/update/"+departamento.numero+"/"+departamento.nombre+"/"+ departamento.localidad} />
</td>
```

Así podemos mandar datos por URL, pero no es recomendable, ya que es peligroso.

## UPDATE con PUT

Para un `UPDATE` es exactamente igual que un `POST`, solo que usamos `axios.put`.

```jsx
updateDepartamento(departamento) {
    return new Promise(function(resolve) {
        let url = Global.urlApiDepartamentos;
        let endpoint = "/api/departamentos";

        axios.put(url + endpoint, departamento).then((response) => {
            resolve(response)
        })
    })
}
```

## DELETE

```jsx
deleteDepartamento(idDepartamento) {
    return new Promise(function(resolve) {
        let url = Global.urlApiDepartamentos;
        let endpoint = "/api/departamentos/" + idDepartamento;

        axios.delete(url + endpoint).then((response) => {
            resolve(response)
        })
    })
}
```
