# REACT CON JS

## Crear proyectos

```bash
npx create-react-app NOMBREPROYECTO
```

Crear proyectos.

```bash
npm start
```

Lanzar el servidor.

```bash
npm install
```

Instalar Librerías.

## Estructura

* `node_modules`: NO es nuestra, son las librerías que tenemos instaladas en nuestro proyecto.
* `package.json`: indica librerías instaladas y versiones. Se utiliza para cuando deseamos sincronizar un proyecto con sus módulos.
* `public`: Esta es la carpeta raíz de los assets o elementos que irán en el navegador. Además, de nuestra página de inicio.
* `src`: Esta carpeta es dónde está la lógica de negocio de nuestro proyecto. Es dónde están los components.

## Proyecto de tipo SPA

**SPA (Single Page Aplication)**

## Components

Los components, dentro de React son ficheros JS y, en su interior contienen tanto la vista como su código Javascript.

### Ejemplo de component

```js
function Saludo(){
    return(
        <div>
            <h1>HOLAAA</h1>
            <h2>QUE TAL</h2>
        </div>
    )
}

export default Saludo;
```
