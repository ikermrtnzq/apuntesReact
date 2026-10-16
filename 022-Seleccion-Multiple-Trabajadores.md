
# SELECCIÓN MÚLTIPLE DE ELEMENTOS

## Selección múltiple de hospitales

```jsx
<select ref={this.selectHospital} className='form-control' size={6} multiple>
    {
        this.state.hospitales.map((hospital, index) => {
            return(
                <option key={index} value={hospital.idHospital}>
                    {hospital.nombre}
                </option>
            )
        })
    }
</select>
```

## Pasar los hospitales seleccionados a otro componente

Luego, cuando hayamos seleccionado los elementos, los pasamos al componente:

```jsx
{
    this.state.hospitalesSeleccionados.length != 0 &&
    (<Trabajadores hospitalesSeleccionados={this.state.hospitalesSeleccionados}/>)
}
```

## Obtener trabajadores desde el servicio

Formateamos los datos en el componente.

Luego, en el servicio, recibimos los datos ya formateados:

```jsx
async ontenerTrabajadores(data) {
    let url = Global.urlApiTrabajadores;
    let endpoint = "/api/trabajadores/trabajadoreshospitales?" + data;

    try {
        let response = await axios.get(url + endpoint);
        return response.data;
    } catch(error) {
        throw error;
    }
}
```
