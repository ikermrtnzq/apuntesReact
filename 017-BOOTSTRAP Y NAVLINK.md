
# BOOTSTRAP Y NAVLINK

Vamos a usar Bootstrap, para ello hay que instalar sus librerías:

```bash
npm install --save bootstrap
npm install --save jquery popper.js
```

Luego en `index.js` hay que aplicar librerías:

```jsx
import 'bootstrap/dist/css/bootstrap.min.css'
import $ from 'jquery';
import Popper from 'popper.js';
import 'bootstrap/dist/js/bootstrap.bundle'
```

Con esas rutas no cumplimos las normas de REACT ya que recargamos pagina, por lo que vamos a usar `NavLink`.

```jsx
<ul>
    <li><NavLink to="/collatz">Collatz</NavLink></li>
</ul>
```

```jsx
<ul>
   <li><NavLink to="/collatz/21">Collatz</NavLink></li>
</ul>
```

## Mover Menu dentro de Router

Para poder usarlo debemos mover componente `Menu` a dentro de `Router`:

```jsx
<BrowserRouter>
    <Menu/>
    <Routes>
```

Así evitamos recargar la página con cada ruta. Para que el contenido se actualice utilizamos `componentDidUpdate`:

```jsx
componentDidUpdate = (oldProps) => {
    if (oldProps.numero != this.props.numero) {
        this.calcularCollatz()
    }
}
```
