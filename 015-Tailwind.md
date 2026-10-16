Instalación y configuración de Tailwind CSS en React
1. Instalación de Tailwind CSS

Este proyecto utiliza React creado con npx create-react-app.

Abrimos una terminal en la carpeta raíz del proyecto y ejecutamos el siguiente comando:

npm install tailwindcss@3

2. Crear el archivo de configuración

Ejecutamos el siguiente comando para generar el archivo tailwind.config.js:

npx tailwindcss init

3. Configurar tailwind.config.js

Abrimos el archivo tailwind.config.js y configuramos las rutas de los archivos donde utilizaremos Tailwind CSS:

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

4. Configurar los estilos CSS

Abrimos el archivo src/index.css y añadimos las siguientes directivas:

@tailwind base;
@tailwind components;
@tailwind utilities;


Estas directivas permiten utilizar las clases de utilidad de Tailwind CSS en los componentes de React.

5. Importar el archivo CSS

Comprobamos que el archivo src/index.js importe la hoja de estilos:

import './index.css';


Si la importación ya existe, no es necesario añadirla de nuevo.

6. Utilizar Tailwind CSS en React

Podemos utilizar las clases de Tailwind directamente en la propiedad className de los elementos JSX.

Ejemplo en src/App.js:

function App() {
  return (
    <div className="p-5">
      <h1 className="text-3xl font-bold text-blue-600">
        Hola, Tailwind CSS
      </h1>
    </div>
  );
}

export default App;

Algunas clases utilizadas
p-5: añade espacio interior.
text-3xl: aumenta el tamaño del texto.
font-bold: establece el texto en negrita.
text-blue-600: aplica un color azul al texto.
7. Ejecutar el proyecto

Para iniciar la aplicación React, ejecutamos:

npm start


Abrimos la dirección que aparece en la terminal para comprobar que los estilos se aplican correctamente.

8. Resumen de comandos
npm install tailwindcss@3
npx tailwindcss init
npm start

9. Resultado

Una vez completada la configuración, podemos utilizar las clases de Tailwind CSS en nuestros componentes React sin necesidad de escribir CSS personalizado para cada estilo.

Nota: esta configuración corresponde a Tailwind CSS v3 y Create React App. Si el proyecto utiliza Tailwind CSS v4, el procedimiento es diferente.
