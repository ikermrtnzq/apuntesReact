# CICLO DE VIDA DE COMPONENTS

El ciclo de vida permite components dinámicos/estáticos.

Los métodos indican cuando se llaman.

## ComponentDidUpdate()

Se ejecuta cuando cambia el render.

## ComponentDidMount()

Se ejecuta antes de dibujar el component y una vez solo.

```js id="2egup0"
componentDidMount = () => {
    this.generarNumeros();
}
```

## ComponentWillUnMount()

Se ejecuta cuando el component es eliminado del Parent.
