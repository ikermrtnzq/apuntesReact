
# CLASES DE SERVICIOS

Sirven para tener en un lugar todas las peticiones. Son clases.

Creamos una carpeta `services` y ahí las clases `.js`. Dentro de cada clase habrá funciones, las cuales van a ser promesas (asíncronas).

## Crear una clase de servicio

```jsx
import Global from '../Global';
import axios from 'axios';

export default class ServiceHospitales {
    getHospitales = new Promise(function(resolve) {
        let url = Global.urlApiHospitales;
        let endpoint = "api/hospitales";

        axios.get(url + endpoint).then((response) => {
            resolve(response.data)
        })
    })
}
```

## Instanciar el servicio desde un componente

Luego, desde un componente, la instanciamos y usamos las funciones:

```jsx
import ServiceHospitales from '../services/ServiceHospitales';

export default class Hospitales extends Component {
    service = new ServiceHospitales();
}
```

## Acceder a las funciones del servicio

```jsx
obtenerHospitales = () => {
    this.service.getHospitales.then(result => {
        this.setState({
            hospitales: result
        })
    })
}
```

## Pasar parámetros a una función

Si queremos pasar parámetros a la función, hacemos la promesa dentro de la función:

```jsx
getDoctoresHospital(id) {
    return new Promise(function(resolve) {
        let url = Global.urlApiDoctores;
        let endpoint = "api/Doctores/DoctoresHospital/";

        axios.get(url + endpoint + id).then((response) => {
            resolve(response.data)
        })
    })
}
```

Y la llamada sería así:

```jsx
buscarDoctores = () => {
    this.service.getDoctoresHospital(this.props.idhospital).then(result => {
        this.setState({
            doctores: result
        })
    })
}
```
