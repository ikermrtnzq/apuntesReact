# REACT ROUTING

```bash
npm install --save react-router-dom
```

SPA utiliza routing entre components.

Routing es habilitar un sitio donde se dibujan los components.

## Router

```js
import {Component} from "react"
import {BrowserRouter, Routes, Route} from "react-router-dom"
import Home from "./Home"
import Musica from "./Musica"

export default class Router extends Component{
    render(){
        return(
            <BrowserRouter>
                <Routes>
                    <Route path="/" element={<Home/>}></Route>
                    <Route path="/musica" element={<Musica/>}></Route>
                </Routes>
            </BrowserRouter>
        )
    }
}
```

## En index.js o componente principal

Ponemos:

```jsx
<Router/>
```

Con el import:

```js
import Router from "./Router"
```

Y:

```js
root.render(
    <Router/>
)
```

El router importado debe ser **nuestro componente**.

## Menú

```jsx
<a href="/">Home</a>
<a href="/cinema">Cinema</a>
<a href="/musica">Musica</a>
```
