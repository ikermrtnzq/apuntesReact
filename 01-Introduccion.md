# ⚛️ React — Introducción

## 📦 Crear un proyecto

Crear un proyecto React:

```bash
npx create-react-app NOMBREPROYECTO
```

Lanzar el servidor:

```bash
npm start
```

Instalar las librerías del proyecto:

```bash
npm install
```

---

# 📁 Estructura del proyecto

## `node_modules`

Contiene las librerías que tenemos instaladas en nuestro proyecto.

> ⚠️ **NO es nuestra carpeta**. Contiene las dependencias/librerías.

---

## `package.json`

Indica:

* Librerías instaladas.
* Versiones de las librerías.

Se utiliza cuando queremos **sincronizar un proyecto con sus módulos**.

---

## `public`

Es la carpeta raíz de los **assets o elementos que irán en el navegador**.

También contiene nuestra página de inicio.

---

## `src`

Contiene la **lógica de negocio** del proyecto.

Aquí se encuentran los **components**.

---

# 🌐 SPA — Single Page Application

React trabaja como una:

**SPA = Single Page Application**

La aplicación se desarrolla mediante componentes que se van mostrando dentro de la aplicación.

---

# 🧩 Componentes

Los componentes dentro de React son **ficheros JS** que contienen:

* La vista.
* El código JavaScript.

## Ejemplo de componente

```jsx
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

---

# 🧠 RESUMEN RÁPIDO

| Elemento               | Para qué sirve                    |
| ---------------------- | --------------------------------- |
| `npx create-react-app` | Crear proyecto                    |
| `npm start`            | Lanzar servidor                   |
| `npm install`          | Instalar librerías                |
| `node_modules`         | Librerías instaladas              |
| `package.json`         | Librerías + versiones             |
| `public`               | Assets / elementos del navegador  |
| `src`                  | Lógica + componentes              |
| SPA                    | Single Page Application           |
| Component              | Fichero JS con vista + JavaScript |

---

# 🔥 CHULETA

```text
CREAR
npx create-react-app NOMBRE

LANZAR
npm start

INSTALAR
npm install

node_modules → librerías
package.json  → librerías + versiones
public        → assets / navegador
src           → lógica + components

SPA = Single Page Application

COMPONENTE:
function Saludo(){
    return(
        <div>
            <h1>HOLAAA</h1>
        </div>
    )
}

export default Saludo;
```
